# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 0.2.1 (UNRELEASED)
### Changed
- Changed repository from [RustCrypto/hashes] to [RustCrypto/XOFs] ([#2])

[RustCrypto/hashes]: https://github.com/RustCrypto/hashes
[RustCrypto/XOFs]: https://github.com/RustCrypto/XOFs

[#2]: https://github.com/RustCrypto/XOFs/pull/2

## 0.2.0 (2026-05-12)
### Added
- `CShake128Reader` and `CShake256Reader` type aliases ([RustCrypto/hashes#855])

### Changed
- Internal implementation by removing unnecessary buffering ([RustCrypto/hashes#849])
- `Rate: BlockSizes` generic parameter to `const RATE: usize` ([RustCrypto/hashes#849])

### Removed
- Implementations of `BlockSizeUser` ([RustCrypto/hashes#856])

[RustCrypto/hashes#849]: https://github.com/RustCrypto/hashes/pull/849
[RustCrypto/hashes#855]: https://github.com/RustCrypto/hashes/pull/855
[RustCrypto/hashes#856]: https://github.com/RustCrypto/hashes/pull/856

## 0.1.1 (2026-04-19)
### Fixed
- Non-compliant initialization when serialized length of function name and customization string
  is a multiple of the block size ([RustCrypto/hashes#834])

[RustCrypto/hashes#834]: https://github.com/RustCrypto/hashes/pull/834

## 0.1.0 (2026-04-13)
- Initial release with implementation moved from the `sha3` crate ([RustCrypto/hashes#815])

[RustCrypto/hashes#815]: https://github.com/RustCrypto/hashes/pull/815
