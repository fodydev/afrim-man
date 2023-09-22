Usage
===

Once you have the `afrim` installed, you can use it.
But before you should download or write your own configuration file.
You can download a official dataset via the [Afrim Dataset Repository](https://github.com/pythonbrad/afrim-data).

Sample configuration file
---
```toml
# config.toml
[core]
buffer_size = 64

[data]
a1 = "à"

[translation]
hi = "hello"
```

Check out the [Configuration Guide](/configuration) for more information about how to write a configuration file.

Demo
---
Considering the sample configuration file above, you can run the afrim with this command `afrim config.toml`.
