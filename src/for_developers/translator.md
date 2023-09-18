Translator
===

A "translator" is simply a program which `clafrica` will invoke during the translation process, allowing you to use programmable predictions. Possible use cases are:
- Auto-correction
- Auto-suggestion

The fact that clafrica utilizes [The Rhai Scripting Language](https://rhai.rs) makes it easy to implement a simple translator.

The following code block shows how to write a translator who suggest a date in another format.

```js
// scripts/datetime/date.rhai
const MONTHS = ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul",  "Aug", "Sep", "Oct", "Nov", "Dec"];

fn parse_cmd(input) {
    let data = input.split('_');
    
    if data.len() == 3 {
    	return data[1];
    }
    
    return "";
}

fn parse_date(input) {
    let data = input.split('/');
    
    if data.len() == 3 {
        let day = parse_int(data[0]);
        let month = parse_int(data[1]);
        let year = parse_int(data[2]);
        
        if day in 1..31 && month in 1..12 && year in 1..2100 {
            return [day, month, year];
        }
    }
    
    return [];
}

// Main function
fn translate(input) {
    let data = core::parse_cmd(input);
    let date = parse_date(data);
    
    if !date.is_empty() {
        return [input, "", [`${date[0]} ${global::MONTHS[date[1]]} ${date[2]}`, `${global::MONTHS[date[1]]} ${date[0]} ${date[2]}`], true];
    }
    
    return [input, "", "", false];
}
```

The most important part of this code, is the `translate` function. All translator should have this function. His signature is as follo:
- input: The current user input (String).
- output: A list of value (Array).
    1. The user input (String).
    2. The remaining code to complete the user input (String).
    3. The translator output (String|Array).
    4. If the translation is ready to use (Boolean).

The syntax of the translator configuration is as below.

```toml
# scripts/datetime/datetime.toml
[translators]
date = "./date.rhai"
time = "./time.rhai"
```
