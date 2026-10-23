# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

## 0.10.0 - 2026-10-23
### Added
- Initial version

### Fixed
- Use the structured `networking.fqdn` fact for `ServerName`, legacy facts such as `fqdn` aren't available in Puppet 8 and later
