# RustCrypto: Extendable Output Functions (XOFs)

[![Project Chat][chat-image]][chat-link]
[![dependency status][deps-image]][deps-link]
![Apache2/MIT licensed][license-image]

Collection of cryptographic [extendable output functions][XOF] written in pure Rust.

All algorithms reside in separate crates and are implemented using traits from [`digest`] crate.
Usage examples are provided in `digest` and hash implementation crate docs.
Additionally all crates do not require the standard library (i.e. `no_std` capable) and can be
easily used for bare-metal or WebAssembly programming by disabling default crate features.

## License

All crates in this repository are licensed under either of

* [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
* [MIT license](http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any additional terms or conditions.

[//]: # (badges)

[chat-image]: https://img.shields.io/badge/zulip-join_chat-blue.svg
[chat-link]: https://rustcrypto.zulipchat.com/#narrow/stream/260041-hashes
[license-image]: https://img.shields.io/badge/license-Apache2.0/MIT-blue.svg
[deps-image]: https://deps.rs/repo/github/RustCrypto/XOFs/status.svg
[deps-link]: https://deps.rs/repo/github/RustCrypto/XOFs

[//]: # (footnotes)

[XOF]: https://en.wikipedia.org/wiki/Extendable-output_function
