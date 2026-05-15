# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## 0.2.1 (2026-05-15)
### Changed
- Repository from [RustCrypto/hashes] to [RustCrypto/XOFs] ([#2])

[RustCrypto/hashes]: https://github.com/RustCrypto/hashes
[RustCrypto/XOFs]: https://github.com/RustCrypto/XOFs

[#2]: https://github.com/RustCrypto/XOFs/pull/2

## 0.2.0 (2026-05-12)
### Changed
- Internal implementation by removing unnecessary buffering ([RustCrypto/hashes#849])
- Serialization format used by `SerializableState` implementations ([RustCrypto/hashes#849])
- Replaced implementation of `CustomizedInit` with `TryCustomizedInit` ([RustCrypto/hashes#857])

[RustCrypto/hashes#849]: https://github.com/RustCrypto/hashes/pull/849
[RustCrypto/hashes#857]: https://github.com/RustCrypto/hashes/pull/857

## 0.1.0 (2026-04-24)
- Initial release ([RustCrypto/hashes#841])

[RustCrypto/hashes#841]: https://github.com/RustCrypto/hashes/pull/841
