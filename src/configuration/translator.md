# Translator Configuration

Here is an example of what the translator configuration might look like.

```toml
# amharic/data/names.toml
[info]
source = "https://github.com/Simonbelete/kwat/blob/main/names/names.csv"
description = "Ethiopic name"
version = "2023-09-15"

[translation]
"Eman" = "ኢማን"
"Addis" = { values = ["ሰኢድ", "አዲስ"], alias = ["EIads", "eiads", "eIads", "Eiads", "Seid"] }
"Shimei" = { value = "ሰሜኢ", alias = ["eIasm", "EIasm", "eiasm", "eiasM", "eIasM", "EiasM", "Eiasm", "EIasM"] }
...
```

We have 4 ways to represent the translator configuration.
- **Simple**: Key - Value representation.
- **Detailed**: Suitable when we want to use alias.
- **More Detailed**: Suitable when we can have many values.
- **Scripting**: Suitable for complex suggestions (date, number, etc.). For more details about it confer [Translator for Developers](/for_developers/translator.md).

