# Github Action Large Pull Request Checker

A Github Action that checks if your Pull Requests exceed a given limit of number of lines of code changes (additions + deletions).

## Usage

```yaml
on: [pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: adolfosilva/gh-large-pr-check@v1.0.0
        with:
          target_branch: ${{ github.event.pull_request.base.href }}
          max_lines_changed: 500
```

## License

This is software is licensed under the MIT license. See [LICENSE](./LICENSE) for details.

