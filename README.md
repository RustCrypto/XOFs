# RustCrypto: Extendable Output Functions (XOFs)

[![Project Chat][chat-image]][chat-link]
[![dependency status][deps-image]][deps-link]
![Apache2/MIT licensed][license-image]

Collection of cryptographic [extendable output functions (XOFs)][XOF] written in pure Rust.

All algorithms reside in separate crates and are implemented using traits from [`digest`] crate.
Usage examples are provided in `digest` and hash implementation crate docs.
Additionally all crates do not require the standard library (i.e. `no_std` capable) and can be
easily used for bare-metal or WebAssembly programming by disabling default crate features.

## Supported Algorithms

|     Algorithm    |       Crate       | Crates.io | Documentation | MSRV |
|------------------|-------------------|:---------:|:-------------:|:----:|
| [Ascon-XOF128]   | [`ascon‑xof128`]  | [![crates.io](https://img.shields.io/crates/v/ascon-xof128.svg)](https://crates.io/crates/ascon-xof128) | [![Documentation](https://docs.rs/ascon-xof128/badge.svg)](https://docs.rs/ascon-xof128) | 1.85 |
| [bash-prg-hash]  | [`bash-prg‑hash`] | [![crates.io](https://img.shields.io/crates/v/bash-prg-hash.svg)](https://crates.io/crates/bash-prg-hash) | [![Documentation](https://docs.rs/bash-prg-hash/badge.svg)](https://docs.rs/bash-prg-hash) | 1.85 |
| [cSHAKE]         | [`cshake`]        | [![crates.io](https://img.shields.io/crates/v/cshake.svg)](https://crates.io/crates/cshake) | [![Documentation](https://docs.rs/cshake/badge.svg)](https://docs.rs/cshake) | 1.85 |
| [KangarooTwelve] | [`k12`]           | [![crates.io](https://img.shields.io/crates/v/k12.svg)](https://crates.io/crates/k12) | [![Documentation](https://docs.rs/k12/badge.svg)](https://docs.rs/k12) | 1.85 |
| [SHAKE]          | [`shake`]         | [![crates.io](https://img.shields.io/crates/v/shake.svg)](https://crates.io/crates/shake) | [![Documentation](https://docs.rs/shake/badge.svg)](https://docs.rs/shake) | 1.85 |
| [TurboSHAKE]     | [`turboshake`]    | [![crates.io](https://img.shields.io/crates/v/turboshake.svg)](https://crates.io/crates/turboshake) | [![Documentation](https://docs.rs/turboshake/badge.svg)](https://docs.rs/turboshake) | 1.85 |

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

[//]: # (crates)

[`ascon‑xof128`]: ./ascon-xof128
[`bash-prg‑hash`]: ./bash-prg-hash
[`cshake`]: ./cshake
[`k12`]: ./k12
[`shake`]: ./shake
[`turboshake`]: ./turboshake

[//]: # (algorithms)

[Ascon-Xof128]: https://doi.org/10.6028/NIST.SP.800-232.ipd
[bash-prg-hash]: http://apmi.bsu.by/assets/files/std/bash-spec241.pdf
[cSHAKE]: https://csrc.nist.gov/pubs/sp/800/185/final
[KangarooTwelve]: https://keccak.team/kangarootwelve.html
[SHAKE]: https://csrc.nist.gov/pubs/fips/202/final
[TurboSHAKE]: https://keccak.team/turboshake.html

[//]: # (footnotes)

[XOF]: https://en.wikipedia.org/wiki/Extendable-output_function
