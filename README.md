# asdf-angular-cli

[![CI](https://img.shields.io/github/actions/workflow/status/dainer88/asdf-angular-cli/test.yml)](https://github.com/dainer88/asdf-angular-cli/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](./LICENSE)

An asdf plugin to manage multiple versions of the Angular CLI ([Angular CLI documentation](https://angular.io/cli)).

## 🚀 Installation

```bash
asdf plugin add angular-cli https://github.com/dainer88/asdf-angular-cli.git
```

## 📦 Usage

```bash
asdf install angular-cli 18.2.1
asdf set angular-cli 18.2.1
ng version
```

## 🧪 Local development and testing

Clone this repository and add the plugin locally:

```bash
git clone https://github.com/dainer88/asdf-angular-cli.git
asdf plugin add angular-cli ./asdf-angular-cli
asdf list all angular-cli
```

To test a specific version:

```bash
asdf install angular-cli 18.2.1
asdf set angular-cli 18.2.1
ng version
```

## 🧰 Requirements

- jq
- curl
- npm or pnpm

## 🧩 Contributing

1. Fork the repository.
2. Create a new branch (`feature/new-feature`).
3. Make your changes and run the tests.
4. Open a Pull Request.

For detailed contribution guidelines, see `CONTRIBUTING.md`.

## 🧪 Automated validation

This repository uses GitHub Actions to validate the plugin scripts and basic syntax.
