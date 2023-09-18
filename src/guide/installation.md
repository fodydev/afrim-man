Installation
===

There are multiple ways to install the clafrica input method. Choose any one of the methods below that best suit your needs.

Pre-compiled binaries 
---
Executable binaries are available for download on the [Github Releases page](https://github.com/pythonbrad/clafrica/releases). Download the binary for your platform (Windows, macOS, or Linux) and extract the archive. The archive contains an `clafrica` executable.

To make it easier to run, put the path to the binary into your `PATH`.

Build from source using Rust
---
To build `clafrica` executable from source, you will first need to install Rust and Cargo. Follow the instructions on the [Rust installation page](https://www.rust-lang.org/tools/install). clafrica currently requires at least Rust version 1.7 for performance.

Once you have installed Rust, the following command can be used to build and install clafrica:

`cargo install clafrica`

This will automatically download clafrica from [crates.io](https://crates.io), build it, and install it in Cargo's global binary directory (~/.cargo/bin/ by default).

To uninstall, run the command `cargo uninstall clafrica`.

Installing the latest master version
---
The version published to crates.io will ever so slightly be behind the version hosted on GitHub. If you need the lastest version, you can build the git version of clafrica yourself. Cargo makes this ***super easy***!

`cargo install --git https://github.com/pythonbrad/clafrica.git clafrica`

Again, make sure to add the Cargo bin directory to your `PATH`.

If you are interested in making modifications to clafrica itself, checkout the [Contributing Guide](https://github.com/pythonbrad/clafrica) for more information.
