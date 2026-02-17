# lint-yaml

A composite action for linting YAML files.

## Usage

```yaml
name: Lint

on: pull_request

permissions:
  contents: read

jobs:
  yamllint:
    name: YAML
    runs-on: ubuntu-24.04
    steps:
      - name: Checkout
        uses: actions/checkout@v6

      - name: Lint YAML Files
        uses: craigsloggett/lint-yaml@v1
```

### Inputs

| Input            | Required? | Default  | Description                                         |
| ---------------- | --------- | -------- | --------------------------------------------------- |
| `python-version` | `false`   | `3.14.2` | The version of Python to use when running yamllint. |
