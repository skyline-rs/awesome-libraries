# Awesome Skyline-Usable Libraries
A list of libraries that have been tested with skyline-rs

## Just Works

These will work just like when used anywhere else.

* Todo

## Made for Skyline

* [skyline-rs](https://github.com/ultimate-research/skyline-rs) - A library for working with Skyline itself and utilities for patching
* [nnsdk-rs](https://github.com/ultimate-research/nnsdk-rs) - Rust bindings to the Nintendo SDK

## Requires Dependency patching

* [rand](https://docs.rs/rand) - Generates random numbers. Requires a patch for `getrandom`

```
[patches.crates-io]
getrandom = { git = "https://github.com/skyline-rs/getrandom" }
```

## Available patches

* [getrandom](https://github.com/skyline-rs/getrandom) - OS-specific random number generator. Depended on by `rand`.

```
[patches.crates-io]
getrandom = { git = "https://github.com/skyline-rs/getrandom" }
```

* [ring](https://github.com/skyline-rs/ring) - Cryptography primatives

```
[patches.crates-io]
ring = { git = "https://github.com/skyline-rs/ring" }
```
