# sqlite: A modern CMake build system for SQLite

<!--
SPDX-FileCopyrightText: 2026 AlgorIT Software Consultancy <https://codeberg.org/algoritnl>
SPDX-License-Identifier: BSL-1.0
-->

[![CI Test](https://github.com/algoritnl/sqlite/actions/workflows/ci-test.yaml/badge.svg)](https://github.com/algoritnl/sqlite/actions/workflows/ci-test.yaml)

A modern CMake build system to build, install, and integrate the official SQLite Amalgamation into C/C++ projects.

## Features

* **Drop-in replacement:** Includes vendored SQLite sources in the `source/` directory.
* **Integrity Verification**: Includes a SHA3-256 checksum file `source/sqlite3.sha3sum` to verify code authenticity.
* **Highly Configurable:** Native CMake options mapping directly to the official SQLite compile-time options.
* **Customizable:** Swap the included sources with a customized SQLite amalgamation if needed.
* **Modern CMake:** Provides standard CMake export targets for seamless integration.

## Usage

After building and installing this project, you can integrate it into your own CMake project using the standard `CONFIG` mode:

```cmake
find_package(sqlite CONFIG REQUIRED)
target_link_libraries(your_target PRIVATE sqlite::sqlite)
```

Other supported integrations include `FetchContent`  and `add_subdirectory`.

## Licensing

This repository uses a dual-license structure:
* The CMake build configurations and tools are licensed under the permissive **BSL-1.0** license.
* The SQLite source code files in the `source/` directory are redistributed under the official **SQLite Blessing** (`blessing`).

## Legal Disclaimer

This repository is an independent open-source project and is not affiliated with, endorsed by, or associated with D. Richard Hipp or the official SQLite contributors. The term "SQLite" and any associated logos are trademarks of Hipp, Wyrick & Company, Inc., and are used in this repository solely for nominative purposes to identify the software being configured and built.
