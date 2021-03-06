#  Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.5] - 2020-02-14
### Fixed
- Fixed an error in which balances did not automatically update on the account screen

### Changed
- Changed fee estimation screen to properly account for how the fee is a rate, not a flat fee per transaction 

## [0.2.4] - 2020-02-14
### Fixed
- Upgraded HSD to a version without mempool issues 

## [0.2.3] - 2020-02-11
### Changed
- Disable airdrop functionality until block 2016
- Made transaction activation alerts dynamic
- Made node start/stop functionality node robust

### Fixed
- Fixed a crash while updating domain name records
- Fixed various minor copy issues

## [0.2.2] - 2020-02-10
### Fixed
- Fixed an issue where chainstate was wiped when mainnet wallets are reset. This means that Bob no longer needs to perform a sync from zero after resetting mainnet wallets
- Fixed an issue where Windows machines might time out restarting Bob
- Fixed an issue where the error displayed when `hsd`'s ports are in use displayed as `undefined` on the splash screen 

## [0.2.1] - 2020-02-03
### Fixed
- Fixed an issue where mainnet wallets could not be regenerated

## [0.2.0] - 2020-02-03
### Added
- Enabled mainnet/testnet networks
- Added support for Windows
- Added a message alerting users that transactions are disabled for the first two weeks following mainnet

### Changed
- `hsd` updated to latest pre-mainnet version
- Record management updated to reflect latest `hsd` changes
    - All record types except `NS`, `DS`, `GLUE4/6`, `SYNTH4/6`, and `TXT` have been removed
- Removed some unused internal methods
- Added release information to Sentry
- Log application crashes on startup to Sentry

### Fixed
- Fix the GitHub link on the Add Funds screen
- Fixed transaction ordering
- Increase FS lock detection timeout

## [0.1.1] - 2020-01-22
### Fixed
- Fixed broken `isDev` flag in analytics service.

### Changed
- Bump `webpack-bundle-analyzer` in response to automatic security vuln [PR #78](https://github.com/kyokan/bob-wallet/pull/78)
    - NOTE: This vulnerability does not affect production Bob clients, since `webpack-bundle-analyzer` is only used for internal build tooling.  

## [0.1.0] - 2020-01-21
### Added

- Initial public beta release
