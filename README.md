# sgrep action

This action runs [sgrep](https://sgrep.dev) and returns the output

## Inputs

### `config`

The config `file|directory|yaml_url|tar|url|registry_name`.

### `targets`

The target(s) to scan

## Example usage

```yaml

name: Sgrep

on: [push]

jobs:
  self_test:
    runs-on: ubuntu-latest
    name: A job to run sgrep
    steps:
      - uses: actions/checkout@v2
      - name: sgrep action step
        id: sgrep
        uses: returntocorp/sgrep-action@master
        with:
          config: './tests/self_test.yml'
          targets: './tests'
```
