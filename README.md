# FLAC

[![Build Status](https://travis-ci.org/sourrust/flac.svg?branch=master)](https://travis-ci.org/sourrust/flac)

An implementation of [FLAC][flac], free lossless audio codec, written in
Rust.

[Documentation][documentation]

## Install

flac is on [crates.io][crates] and can be included in your Cargo file
like so:

```toml
[dependencies]

flac = "^0.3.0"
```

Followed by including it in you code:

```rust
extern crate flac;
```

## Implementation Status

The status of this FLAC implementation:

Currently this project fully parsers every FLAC file I've throw at it
and the decoding working great for any file that has a bit sample size
of 16 and before. This is based on the test suite I have on this project
and the test do fail when bit sample size is larger than 16.

Currently I'm trying to get the decoder to use varied sized integers in
order for the allocations of buffers to be more efficient and afterward
I want to start on that encoding side of FLAC. It will be a bit slower
as I am busy with work but that is a goal of the project for sure.

- [ ] encoder

[flac]: https://xiph.org/flac
[documentation]: https://sourrust.github.io/flac
[crates]: https://crates.io/crates/flac/
