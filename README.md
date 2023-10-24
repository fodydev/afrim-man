<div align="center">

  <h1>The Afrim Book</h1>

  <strong>This small book describes how to use afrim.</strong>

  <h3>
    <a href="https://pythonbrad.github.io/afrim-man/">Read the Book</a>
    <span> | </span>
    <a href="https://github.com/pythonbrad/afrim/blob/main/CONTRIBUTING.md">Contributing</a>
  </h3>

  <sub>Built with 🦀🕸</sub>
</div>

## About

This repo contains documentation on using afrim, how
to get started and more as you dive deeper. It acts as a guide for doing some really neat things with afrim.

If you would like to start learning how to use afrim,
 you can read the book [online here][book].

[Open issues for improving the Afrim book.][book-issues]

## Building the Book

The book is made using [`mdbook`][mdbook]. To install it you'll need `cargo`
installed. If you don't have any Rust tooling installed, you'll need to install
[`rustup`][rustup] first. Follow the instructions on the site in order to get
setup.

Once you have that done then just do the following:

```bash
$ cargo install mdbook
```

Make sure the `cargo install` directory is in your `$PATH` so that you can run
the binary.

Now just run this command from this directory:

```bash
$ mdbook build
```

This will build the book and output files into a directory called `book`. From
there you can navigate to the `index.html` file to view it in your browser. You
could also run the following command to automatically generate changes if you
want to look at changes you might be making to it:

```bash
$ mdbook serve
```

This will automatically generate the files as you make changes and serves them
locally so you can view them easily without having to call `build` every time.

The files are all written in Markdown so if you don't want to generate the book
to read them then you can read them from the `src` directory.

[mdbook]: https://github.com/rust-lang-nursery/mdBook
[rustup]: https://github.com/rust-lang-nursery/rustup.rs/
[book]: https://pythonbrad.github.io/afrim-man
[book-issues]: https://github.com/pythonbrad/afrim-man/issues
