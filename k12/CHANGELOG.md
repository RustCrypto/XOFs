# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 0.5.1 (2026-05-15)
### Changed
- Repository from [RustCrypto/hashes] to [RustCrypto/XOFs] ([#2])

[RustCrypto/hashes]: https://github.com/RustCrypto/hashes
[RustCrypto/XOFs]: https://github.com/RustCrypto/XOFs

[#2]: https://github.com/RustCrypto/XOFs/pull/2

## 0.5.0 (2026-05-12)
### Changed
- Internal implementation by removing unnecessary buffering ([RustCrypto/hashes#849])
- `Rate: BlockSizes` generic parameter to `const RATE: usize` ([RustCrypto/hashes#849])

### Removed
- Implementations of `BlockSizeUser` ([RustCrypto/hashes#856])

[RustCrypto/hashes#849]: https://github.com/RustCrypto/hashes/pull/849
[RustCrypto/hashes#856]: https://github.com/RustCrypto/hashes/pull/856

## 0.4.0 (2026-04-24)
### Added
- `alloc` crate feature ([#678])
- `Kt`, `Kt128` and `Kt256` non-customizable types ([RustCrypto/hashes#839])
- `custom` module with customizable variants ([RustCrypto/hashes#839])

### Changed
- Edition changed to 2024 and MSRV bumped to 1.85 ([RustCrypto/hashes#652])
- Relax MSRV policy and allow MSRV bumps in patch releases
- Update to `digest` v0.11
- New implementation with parallel processing support ([RustCrypto/hashes#839])

### Removed
- `std` crate feature ([RustCrypto/hashes#678])
- `KangarooTwelve*` types ([RustCrypto/hashes#839])

[RustCrypto/hashes#652]: https://github.com/RustCrypto/hashes/pull/652
[RustCrypto/hashes#678]: https://github.com/RustCrypto/hashes/pull/678
[RustCrypto/hashes#839]: https://github.com/RustCrypto/hashes/pull/839

## 0.3.0 (2023-06-10)
### Added
- Support for heapless `no_std` targets ([RustCrypto/hashes#353])

### Changed
- Use TurboSHAKE implementation from `sha3` ([RustCrypto/hashes#353])
- Properly implement `XofReader` ([RustCrypto/hashes#353])
- 2021 edition upgrade; MSRV 1.56 ([RustCrypto/hashes#487])

[RustCrypto/hashes#353]: https://github.com/RustCrypto/hashes/pull/353
[RustCrypto/hashes#487]: https://github.com/RustCrypto/hashes/pull/487

## 0.2.1 (2022-02-17)
### Fixed
- Minimal versions build ([RustCrypto/hashes#363])

[RustCrypto/hashes#363]: https://github.com/RustCrypto/hashes/pull/363

## 0.2.0 (2021-12-07)
### Changed
- Update to `digest` v0.10 ([RustCrypto/hashes#217])

[RustCrypto/hashes#217]: https://github.com/RustCrypto/hashes/pull/217

## 0.1.0 (2020-06-09)
### Changed
- Update to `digest` v0.9 release; MSRV 1.41+ ([RustCrypto/hashes#155])
- Use `digest` crate's `alloc` feature ([RustCrypto/hashes#150])
- Impl the `ExtendableOutput` trait ([RustCrypto/hashes#149])
- Rename `*result*` to `finalize` ([RustCrypto/hashes#148])
- Upgrade to Rust 2018 edition ([RustCrypto/hashes#123])

[RustCrypto/hashes#155]: https://github.com/RustCrypto/hashes/pull/155
[RustCrypto/hashes#150]: https://github.com/RustCrypto/hashes/pull/150
[RustCrypto/hashes#149]: https://github.com/RustCrypto/hashes/pull/149
[RustCrypto/hashes#148]: https://github.com/RustCrypto/hashes/pull/148
[RustCrypto/hashes#123]: https://github.com/RustCrypto/hashes/pull/123

## 0.0.1 (2020-05-24)
- Initial release
