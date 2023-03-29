# action-cassette-deck

Used to automatically merge PRs in a second repository

## Usage

### Basic

```yaml

name: Cassette Merge

# only trigger on pull request closed events
on:
  pull_request:
    types: [ closed ]
    

jobs:
  merge:
    runs-on: ubuntu-latest
    steps:
      - uses: rotki/action-cassette-deck@v1
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          cassette_repo: test-caching

```


## License

[AGPL-3.0](./LICENSE) License &copy; 2023- [Rotki Solutions GmbH](https://github.com/rotki)