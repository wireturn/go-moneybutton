# go-moneybutton
> The unofficial golang implementation for the [MoneyButton API](https://docs.moneybutton.com/docs/api-overview.html)

[![Release](https://img.shields.io/github/release-pre/tonicpow/go-moneybutton.svg?logo=github&style=flat&v=3)](https://github.com/tonicpow/go-moneybutton/releases)
[![Build Status](https://img.shields.io/github/workflow/status/tonicpow/go-moneybutton/run-go-tests?logo=github&v=3)](https://github.com/tonicpow/go-moneybutton/actions)
[![Report](https://goreportcard.com/badge/github.com/tonicpow/go-moneybutton?style=flat&v=3)](https://goreportcard.com/report/github.com/tonicpow/go-moneybutton)
[![codecov](https://codecov.io/gh/tonicpow/go-moneybutton/branch/master/graph/badge.svg?v=3)](https://codecov.io/gh/tonicpow/go-moneybutton)
[![Go](https://img.shields.io/github/go-mod/go-version/tonicpow/go-moneybutton?v=3)](https://golang.org/)

<br/>

## Table of Contents

- [Installation](#installation)
- [Documentation](#documentation)
- [Examples & Tests](#examples--tests)
- [Benchmarks](#benchmarks)
- [Code Standards](#code-standards)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contributing](#contributing)
- [License](#license)

<br/>

## Installation

**go-moneybutton** requires a [supported release of Go](https://golang.org/doc/devel/release.html#policy).

```shell script
go get -u github.com/tonicpow/go-moneybutton
```

<br/>

## Documentation

View the generated [documentation](https://pkg.go.dev/github.com/tonicpow/go-moneybutton)

[![GoDoc](https://godoc.org/github.com/tonicpow/go-moneybutton?status.svg&style=flat&v=3)](https://pkg.go.dev/github.com/tonicpow/go-moneybutton)

### Features

- Current coverage for the [MoneyButton API](https://docs.moneybutton.com/docs/api-overview.html)
  - [x] Get Refresh Token
  - [x] Refresh Access Token
  - [x] User Profile
  - [x] User Identity
  - [ ] User Balance
  - [ ] Get Payment By ID
  - [ ] Get Payments

<details>
<summary><strong><code>Library Deployment</code></strong></summary>
<br/>

[goreleaser](https://github.com/goreleaser/goreleaser) for easy binary or library deployment to Github and can be installed via: `brew install goreleaser`.

The [.goreleaser.yml](.goreleaser.yml) file is used to configure [goreleaser](https://github.com/goreleaser/goreleaser).

Use `make release-snap` to create a snapshot version of the release, and finally `make release` to ship to production.

</details>

<details>
<summary><strong><code>Makefile Commands</code></strong></summary>
<br/>

View all `makefile` commands

```shell script
make help
```

List of all current commands:

```text
clean                Remove previous builds and any test cache data
clean-mods           Remove all the Go mod cache
coverage             Shows the test coverage
godocs               Sync the latest tag with GoDocs
help                 Show this help message
install              Install the application
install-go           Install the application (Using Native Go)
lint                 Run the golangci-lint application (install if not found)
release              Full production release (creates release in Github)
release              Runs common.release then runs godocs
release-snap         Test the full release (build binaries)
release-test         Full production test release (everything except deploy)
replace-version      Replaces the version in HTML/JS (pre-deploy)
tag                  Generate a new tag and push (tag version=0.0.0)
tag-remove           Remove a tag if found (tag-remove version=0.0.0)
tag-update           Update an existing tag to current commit (tag-update version=0.0.0)
test                 Runs vet, lint and ALL tests
test-ci              Runs all tests via CI (exports coverage)
test-ci-no-race      Runs all tests via CI (no race) (exports coverage)
test-ci-short        Runs unit tests via CI (exports coverage)
test-short           Runs vet, lint and tests (excludes integration tests)
uninstall            Uninstall the application (and remove files)
update-linter        Update the golangci-lint package (macOS only)
vet                  Run the Go vet application
```

</details>

<br/>

## Examples & Tests
All unit tests and [examples](examples) run via [Github Actions](https://github.com/tonicpow/go-handcash-connect/actions) and
uses [Go version 1.15.x](https://golang.org/doc/go1.15). View the [configuration file](.github/workflows/run-tests.yml).

Run all tests (including integration tests)
```shell script
make test
```

Run tests (excluding integration tests)
```shell script
make test-short
```

<br/>

## Benchmarks

Run the Go [benchmarks](client_test.go):

```shell script
make bench
```

<br/>

## Code Standards

Read more about this Go project's [code standards](CODE_STANDARDS.md).

<br/>

## Usage

View the [examples](examples)

<br/>

## Maintainers

| [<img src="https://github.com/mrz1836.png" height="50" alt="MrZ" />](https://github.com/mrz1836) | [<img src="https://github.com/rohenaz.png" height="50" alt="Satchmo" />](https://github.com/rohenaz) |
| :----------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------: |
|                                [MrZ](https://github.com/mrz1836)                                 |                                [Satchmo](https://github.com/rohenaz)                                 |

<br/>

## Contributing

View the [contributing guidelines](CONTRIBUTING.md) and please follow the [code of conduct](CODE_OF_CONDUCT.md).

## License

![License](https://img.shields.io/github/license/tonicpow/go-moneybutton.svg?style=flat&v=3)
