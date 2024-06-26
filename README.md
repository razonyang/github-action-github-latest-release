# GitHub Latest Release Action

## Usage

```yaml
on: [push]

jobs:
  github_latest_release_job:
    runs-on: ubuntu-latest
    steps:
      - id: release # used to read version in other steps.
        uses: razonyang/github-action-github-latest-release@v1
        with:
          owner: razonyang
          name: foo-bar-fizz-buzz
          # prefix: v # remove prefix from version if present.
      - run: echo ${{ steps.release.outputs.version }}
```
