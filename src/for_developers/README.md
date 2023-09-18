For developers
===

While `clafrica` is mainly used as a binary application, you can also import the core library directly and use that to build your own input method. It also support the [Rhai scripting language](https://rhai.rs) for some customization.

The **For Developers** chapters are here to show you the more advanced usage of `clafrica`.

The two main ways a developer can hook into the clafrica working is via,
- [Processor](./processor.md)
- [Translator](./translator.md)
- [Frontend](./frontend.md)

The Clafrica Working
---
The working of the clafrica goes through several steps.

1. Listening keyboard events
    - Identify the event
    - Identify the operation to perform
2. For each translator:
    1. Perform the translation
    2. Return the predicates
3. Display useful information through the frontend interface

Using clafrica as a Library
---
The `clafrica` binary is based on the `clafrica-lib` crate, exposing its functionality as a input method engine. As such it is quite easy to create your own input method.

The easiest way to find out how to use the `clafrica-lib` crate is by looking at the [API Docs](https://docs.rs/clafrica-lib).
