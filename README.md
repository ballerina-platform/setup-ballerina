[![Test Ubuntu](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-ubuntu.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-ubuntu.yml)
[![Test Windows](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-windows.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-windows.yml)
[![Test Action](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-macos.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-macos.yml)
[![GitHub license](https://img.shields.io/github/license/ballerina-platform/setup-ballerina)](https://github.com/ballerina-platform/setup-ballerina/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/ballerina-platform/setup-ballerina)](https://github.com/ballerina-platform/setup-ballerina/issues)

# Setup Ballerina

This Github action installs [Ballerina](https://ballerina.io)'s build system and package manager command; the `bal` command.

## Inputs

|Input| Description|Required|
|---|---|---|
|_version_|Ballerina SwanLake Version|yes|

## Usage

_**Note**: This action is supported on all operating systems (`ubuntu`, `macos`, `windows`)_

### Ubuntu

```yaml
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: ballerina-platform/setup-ballerina@v1
        name: Install Ballerina
        with:
          version: 2201.1.1
      - run: bal version
      - run: bal run hello.bal
```

[![Test Ubuntu](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-ubuntu.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-ubuntu.yml)
[![Source](https://img.shields.io/badge/-Source-blue)](https://github.com/ballerina-platform/setup-ballerina/blob/main/.github/workflows/test-ubuntu.yml)

### MacOs

```yaml
    runs-on: macos-latest
    steps:
      - uses: actions/checkout@v2
      - uses: ballerina-platform/setup-ballerina@v1
        name: Install Ballerina
        with:
          version: 2201.1.1
      - run: bal version
      - run: bal run hello.bal
```

[![Test Action](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-macos.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-macos.yml)
[![Source](https://img.shields.io/badge/-Source-blue)](https://github.com/ballerina-platform/setup-ballerina/blob/main/.github/workflows/test-macos.yml)

### Windows

```yaml
    runs-on: windows-latest
    steps:
      - uses: actions/checkout@v2
      - uses: ballerina-platform/setup-ballerina@v1
        name: Install Ballerina
        with:
          version: 2201.1.1
      - run: bal version
      - run: bal run hello.bal
```

[![Test Windows](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-windows.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test-windows.yml)
[![Source](https://img.shields.io/badge/-Source-blue)](https://github.com/ballerina-platform/setup-ballerina/blob/main/.github/workflows/test-windows.yml)

## License
The scripts and documentation in this project are released under the [Apache License](https://github.com/ballerina-platform/setup-ballerina/blob/main/LICENSE).