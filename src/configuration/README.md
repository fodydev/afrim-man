Configuration
===

This section details how to write a configuration file.

Here is an example of what a configuration file might look like:

```toml
# amharic-ime/config/conf.toml
[core]
buffer_size     = 64
page_size       = 16
auto_commit     = false

[translators]
geez_numerals   = "../data/geez/scripts/numerals.rhai"

[translation]
amharic_words   = { path = "../data/amharic/dictionary.toml" }
amharic_names   = { path = "../data/amharic/names.toml" }

[data]
geez            = { path = "../data/geez/code.toml" }
```

Supported configuration options
---
It's important to note that **any** relative path specified in the configuration will always be taken from the path where the configuration file is located.

- [Core](/configuration/core.md) configuration to modify the internal behavior of the clafrica.
- [Data](/configuration/data.md) configuration to setup a sequential coding system.
- [Translator](/configuration/translator.md) configuration for auto-suggestions.

