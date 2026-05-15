# RustCrypto: KangarooTwelve

[![crate][crate-image]][crate-link]
[![Docs][docs-image]][docs-link]
![Apache2/MIT licensed][license-image]
![Rust Version][rustc-image]
[![Build Status][build-image]][build-link]

Pure Rust implementation of the [KangarooTwelve] family of extendable-output functions (XOF).

## Examples

KangarooTwelve functions have an extendable output, so finalization methods return
XOF reader from which results of arbitrary length can be read:

```rust
use k12::{Kt128, Update, ExtendableOutput, XofReader};
use hex_literal::hex;

let mut hasher = Kt128::default();
hasher.update(b"abc");
let mut reader = hasher.finalize_xof();
let mut buf = [0u8; 10];
reader.read(&mut buf);
assert_eq!(buf, hex!("ab174f328c55a5510b0b"));
reader.read(&mut buf);
assert_eq!(buf, hex!("209791bf8b60e801a7cf"));
```

Additionally, KangarooTwelve supports customization:

```rust
use k12::{CustomRefKt128, Update, ExtendableOutput, XofReader};
use hex_literal::hex;

let mut hasher = CustomRefKt128::new_customized(b"my customization string");
hasher.update(b"abc");
let mut reader = hasher.finalize_xof();
let mut buf = [0u8; 10];
reader.read(&mut buf);
assert_eq!(buf, hex!("fbe2ce557c1b115bfe1f"));
reader.read(&mut buf);
assert_eq!(buf, hex!("c9d7b4097c55f0f5ae86"));
```

`CustomRefKt128/256` keep reference to the customization string, while `CustomKt128/256`
keep an owned copy of it. Note that the latter types are gated on the `alloc` crate feature.

See the [`digest`] crate docs for additional examples.

## License

The crate is licensed under either of:

* [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
* [MIT license](http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.

[//]: # (badges)

[crate-image]: https://img.shields.io/crates/v/k12.svg
[crate-link]: https://crates.io/crates/k12
[docs-image]: https://docs.rs/k12/badge.svg
[docs-link]: https://docs.rs/k12/
[license-image]: https://img.shields.io/badge/license-Apache2.0/MIT-blue.svg
[rustc-image]: https://img.shields.io/badge/rustc-1.85+-blue.svg
[chat-image]: https://img.shields.io/badge/zulip-join_chat-blue.svg
[chat-link]: https://rustcrypto.zulipchat.com/#narrow/stream/260041-hashes
[build-image]: https://github.com/RustCrypto/XOFs/actions/workflows/k12.yml/badge.svg?branch=master
[build-link]: https://github.com/RustCrypto/XOFs/actions/workflows/k12.yml?query=branch:master

[//]: # (general links)

[KangarooTwelve]: https://keccak.team/kangarootwelve.html
[`digest`]: https://docs.rs/digest
