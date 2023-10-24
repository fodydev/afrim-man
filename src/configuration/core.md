# Core configuration

Here is an example of what the core configuration might look like.

```toml
# afrim/conf/conf.toml
[core]
buffer_size     = 64
page_size       = 16
auto_commit     = false
auto_capitalize = false
```

- **buffer_size**: The memory allowed to the input text.
- **page_size**: The maximun number of suggestions that should be display.
- **auto_commit**: Tell to afrim if the first suggestion got, should be submitted or not.
- **auto_capitalize**: Tell to afrim to generate the capitalize version of the sequential coding system of the current configuration file.

**NB**: Only the core configuration at the root configuration file is considered (except for the `auto_capitalize` field who is file oriented).

