# pre-commit hooks action

[![test pre-commit-action](https://github.com/dym-ok/pre-commit-action/actions/workflows/test.yml/badge.svg)](https://github.com/dym-ok/pre-commit-action/actions/workflows/test.yml)

This GitHub action runs [pre-commit]() hooks in code quality and linting workflows.

## Examples of usage

Add a [.pre-commit-config.yaml](https://pre-commit.com/index.html#2-add-a-pre-commit-configuration)
file to your GitHub project and create a GitHub workflow like this:

```yaml
name: Code Quality
on:
  pull_request:
  push:
    branches:
      - main

jobs:
  linting:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: dym-ok/pre-commit-action@v1

```
