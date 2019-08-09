# Changelog
All notable changes to Pronghorn will be documented in this file.

## [0.0.1] - 2019-08-07
### Changed
- Added per user cgroup restrictions to the login nodes. Each user-${UID}.slice is
  set to CPUShares=1024 and MemoryLimit=32G. This limits each user to roughly
  1 core, if the system is at max load, and 32GiB of RAM.


### Added
TODO
