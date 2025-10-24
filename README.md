# asdf-angular-cli

[![CI](https://img.shields.io/github/actions/workflow/status/dainer88/asdf-angular/test.yml)](https://img.shields.io/github/actions/workflow/status/dainer88/asdf-angular/test.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](./LICENSE)

An asdf plugin to manage multiple versions of the Angular CLI ([Angular CLI documentation](https://angular.io/cli)).

## 🚀 Installation

```bash
asdf plugin-add angular-cli https://github.com/<your-username>/asdf-angular-cli.git
```

## 📦 Usage

```bash
asdf install angular-cli 18.2.1
asdf global angular-cli 18.2.1
ng version
```

## 🧪 Local development and testing

Clone this repository and add the plugin locally:

```bash
git clone https://github.com/<your-username>/asdf-angular-cli.git
asdf plugin-add angular-cli ./asdf-angular-cli
asdf list-all angular-cli
```

To test a specific version:

```bash
asdf install angular-cli 18.2.1
asdf global angular-cli 18.2.1
ng version
```

## 🧰 Requirements

- jq
- curl
- npm

## 🧩 Contributing

1. Fork the repository.
2. Create a new branch (`feature/new-feature`).
3. Make your changes and run the tests.
4. Open a Pull Request.

For detailed contribution guidelines, see `CONTRIBUTING.md`.

## 🧪 Automated validation

This repository uses GitHub Actions to validate the plugin scripts and basic syntax.
