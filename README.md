# Awesome Skyline-Usable Libraries
A list of libraries that have been tested with skyline-rs

## Just Works

These will work just like when used anywhere else.

* Todo

## Made for Skyline

* [skyline-rs](https://github.com/ultimate-research/skyline-rs) - A library for working with Skyline itself and utilities for patching
* [nnsdk-rs](https://github.com/ultimate-research/nnsdk-rs) - Rust bindings to the Nintendo SDK
* [libc-nnsdk](https://github.com/ultimate-research/libc-nnsdk) - ([docs](https://ultimate-research.github.io/skyline-rs-template/doc/libc/index.html)) libc bindings for functions/types exposed by the Nintendo SDK

## Requires Dependency patching

* [rand](https://docs.rs/rand) - Generates random numbers. Requires a patch for `getrandom`

```
[dependencies]
rand = { git = "https://github.com/skyline-rs/rand" }

[patch.crates-io]
getrandom = { git = "https://github.com/skyline-rs/getrandom" }
```

* [rayon](https://docs.rs/rayon) - Makes parallelism as easy as using a iterator

```
[patch.crates-io]
num_cpus = { git = "https://github.com/skyline-rs/num_cpus" }
```

## Game-Specific

### Smash
  - [skyline_smash](https://github.com/ultimate-research/skyline-smash) ([docs](https://ultimate-research.github.io/skyline-rs-template/doc/smash/index.html))
  - [
## Available patches

* [getrandom](https://github.com/skyline-rs/getrandom) - OS-specific random number generator. Depended on by `rand`.

```
[patch.crates-io]
getrandom = { git = "https://github.com/skyline-rs/getrandom" }
```

* [ring](https://github.com/skyline-rs/ring) - Cryptography primatives

```
[patch.crates-io]
ring = { git = "https://github.com/skyline-rs/ring", rev = "d9674965" }
```

* [thread-id](https://github.com/skyline-rs/thread-id) - Getting a unique number for the current thread

```
[patch.crates-io]
thread-id = { git = "https://github.com/skyline-rs/thread-id" }
```
