# semantic-pr-composite-action

This is [GitHub Action composite](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action) that ensure that your PR title matches the ViacomCBS [Conventional Commits spec](https://www.conventionalcommits.org/).

## Usage example

```yml
name: "Lint PR"

on:
  pull_request_target:
    types:
      - opened
      - edited
      - synchronize

jobs:
  main:
    runs-on: ubuntu-latest
    steps:
      - uses: vc-vantage/semantic-pr-composite-action@v1
        with:
          jira-ticket-prefix: 'VPM-'
```
