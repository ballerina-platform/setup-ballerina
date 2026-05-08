[![Test](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test.yml/badge.svg?branch=main)](https://github.com/ballerina-platform/setup-ballerina/actions/workflows/test.yml)
[![GitHub license](https://img.shields.io/github/license/ballerina-platform/setup-ballerina)](https://github.com/ballerina-platform/setup-ballerina/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/ballerina-platform/setup-ballerina)](https://github.com/ballerina-platform/setup-ballerina/issues)

# Setup Ballerina

GitHub Action for installing [Ballerina](https://ballerina.io) and making the `bal` command available in GitHub Actions workflows. The action sets `BALLERINA_HOME` and updates `PATH` for the configured runner.

## Inputs

| Input | Description | Required |
|---|---|---:|
| `version` | Ballerina Swan Lake version to install. Use a fixed version such as `2201.13.3`, or `latest`. Nightly versions are supported with values that start with `nightly`. | Yes |
| `github-token` | GitHub token used only when downloading GitHub Actions artifacts for nightly builds. | No |

## Usage

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set Up Ballerina
        uses: ballerina-platform/setup-ballerina@v1.1.4
        with:
          version: 2201.13.3
      - run: bal run
```

## Supported Runners

This action runs on:

- Ubuntu
- macOS
- Windows

## Troubleshooting

### `bal` command not found

Check that the setup step completed successfully before running `bal` commands. The setup step must run before any step that calls `bal`.

### Version download failed

Check that the configured `version` exists in the [Ballerina Swan Lake archived versions](https://ballerina.io/downloads/archived/#swan-lake-archived-versions). Invalid or unavailable versions cannot be downloaded from `dist.ballerina.io`.

### Nightly download failed

Nightly versions are downloaded from GitHub Actions artifacts in `ballerina-platform/ballerina-distribution` and may require a valid `github-token`.

## License

This project is licensed under the Apache License 2.0. See [LICENSE](LICENSE).
