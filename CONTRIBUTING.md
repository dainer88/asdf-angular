# Contributing to asdf-angular-cli

Thank you for your interest in contributing! This document describes the preferred workflow, coding standards, and checks we expect contributors to follow. Please read it before opening issues or pull requests.

## Table of contents

- How to report an issue
- How to propose a change (pull request)
- Branch naming and commit message conventions
- Development & testing
- Pull request checklist
- Code of Conduct

## How to report an issue

If you find a bug or want to request a feature, open an issue and include:

- A short, descriptive title
- The steps to reproduce (for bugs)
- Expected vs actual behavior
- Environment information (OS, Node/npm versions)
- Any relevant logs or error messages

Use labels to categorize issues when possible.

## How to propose a change (pull request)

1. Fork the repository.
2. Create a branch from `master` using a descriptive name (see Branch naming below).
3. Make your changes in the branch. Keep changes small and focused.
4. Run the tests and basic script checks locally.
5. Open a Pull Request against the `master` branch with a clear description of the change and motivation.

If your changes address an open issue, reference it in the PR (e.g., `Closes #123`).

## Branch naming and commit message conventions

- Branch names should be prefixed with the type and a short description, for example:
  - `feature/add-list-all-cache`
  - `fix/install-permissions`
  - `chore/update-deps`

- Commit messages should follow the Conventional Commits style for clarity. Example:
  - `feat: add list-all cache to reduce registry calls`
  - `fix: handle missing npm gracefully`

This helps with automated changelog generation and clear history.

## Development & testing

This repository contains a set of shell scripts used by the asdf plugin. Basic checks you can run locally:

- Syntax-check shell scripts:

```bash
bash -n bin/install bin/list-all bin/exec
```

- Preview available versions (requires `jq` and `curl`):

```bash
bash bin/list-all | head -n 10
```

- Install a version into a temporary directory (this will install packages with npm):

```bash
mkdir -p /tmp/asdf-angular-cli
bash bin/install 18.2.1 /tmp/asdf-angular-cli
/tmp/asdf-angular-cli/ng version
```

Notes:

- Ensure `npm`, `curl`, and `jq` are installed when running the scripts.
- Keep changes portable and POSIX-compliant where reasonable (this repo targets common Linux and macOS runners).

## Pull request checklist

Before marking your PR ready for review, please ensure:

- [ ] The change is limited in scope and well-documented in the PR description.
- [ ] All shell scripts pass a syntax check (`bash -n`).
- [ ] Any new behavior includes tests or a manual verification step described in the PR.
- [ ] CI (GitHub Actions) passes for all targeted OS runners.
- [ ] The PR has at least one reviewer (maintainers will review when available).

## Code of Conduct

By participating in this project you agree to abide by the Contributor Covenant Code of Conduct. Please be respectful and constructive.

---

If you have questions about contributing, open an issue and tag it `help wanted` or `discussion`.
