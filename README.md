[![Test Action](https://github.com/hasithaa/ballerina-setup/actions/workflows/selftest.yml/badge.svg?branch=main)](https://github.com/hasithaa/ballerina-setup/actions/workflows/selftest.yml)
[![GitHub license](https://img.shields.io/github/license/hasithaa/ballerina-setup)](https://github.com/hasithaa/ballerina-setup/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/hasithaa/ballerina-setup)](https://github.com/hasithaa/ballerina-setup/issues)

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
      - uses: hasithaa/setup-ballerina@v1
        name: Install Ballerina
        with:
          version: 2201.1.1
      - run: bal version
      - run: bal run hello.bal
```

### MacOs

```yaml
    runs-on: macos-latest
    steps:
      - uses: actions/checkout@v2
      - uses: hasithaa/setup-ballerina@v1
        name: Install Ballerina
        with:
          version: 2201.1.1
      - run: bal version
      - run: bal run hello.bal
```

### Windows

```yaml
    runs-on: windows-latest
    steps:
      - uses: actions/checkout@v2
      - uses: hasithaa/setup-ballerina@v1
        name: Install Ballerina
        with:
          version: 2201.1.1
      - run: bal version
      - run: bal run hello.bal
```

## License
The scripts and documentation in this project are released under the [Apache License](https://github.com/hasithaa/setup-ballerina/blob/main/LICENSE).