# `naught`

Naught is a an experimental alternative to [`cargo cross`]. It makes a couple different design decisions:

1. Naught does not provide pre-built versions of dockerized cross-compilation environments. Users will need to build the docker image locally before the first use.
2. Naught focuses on community driven cross-compilation environments. Read below for more information.
3. For now, only cross compilation is supported. Emulation for the purposes of testing is a non-goal at the moment.

[`cargo cross`]: https://github.com/rust-embedded/cross

## `Dockerfile` library

You can find the library of cross-compilation dockerfiles in the [`naught-library`] repo.

Similar to [`cargo cross`], cross-compilation environments are defined as `Dockerfile`s, and cross compilation is executed within a docker container.

In `cargo cross`, maximal backwards compatibility was a primary target. Naught instead has no focus. Users may submit dockerfiles to be part of the "library", though no official support is given to environments in this library. Only the Naught tool itself will be supported.

We suggest that users provide different environments for different use cases: some for maximal backwards compatibility, some for maximal convenience with many modern libraries pre-installed, etc.

[`naught-library`]: https://github.com/jamesmunns/naught-library
