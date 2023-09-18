# Data Configuration

Here is an example of what the data configuration might look like.

```toml
# clafrica/data/clafrica_double.toml
[info]
name		=   "Clafrica double"
description =   "Clafrica code for speed typing of double characters"
authors		=   ["Resulam <contact@resulam.com>"]
website		=   "https://resulam.com"
version		=   "2023-07-06"

[data]
"a11"		=   { value = "àà", alias = ["1aa", "aa1"] }
"a22"		=	{ value = "áá", alias = ["2aa", "aa2"] }
"a33"		=	{ value = "āā", alias = ["3aa", "aa3"] }
"a55"		=	{ value = "ââ", alias = ["5aa", "aa5"] }
"a77"		=	{ value = "ǎǎ", alias = ["7aa", "aa7"] }

"aff"		=	"ɑɑ"
"aff1"		=	{ value = "ɑ̀ɑ̀", alias = ["1aff", "af11"] }
"aff2"		=	{ value = "ɑ́ɑ́", alias = ["2aff", "af22"] }
"aff3"		=	{ value = "ɑ̄ɑ̄", alias = ["3aff", "af33"] }
"aff5"		=	{ value = "ɑ̂ɑ̂", alias = ["5aff", "af55"] }
"aff7"		=	{ value = "ɑ̌ɑ̌", alias = ["7aff", "af77"] }
...
```

We can see that there is two ways to represent data.
- **Simple**: Key - Value representation.
- **Detailed**: Suitable for code with alias.

