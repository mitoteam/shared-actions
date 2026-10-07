# MiTo Team shared actions

![GitHub](https://img.shields.io/github/license/mitoteam/shared-actions)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/y/mitoteam/shared-actions)](https://github.com/mitoteam/shared-actions/commits)


GitHub Workflows to use in other projects

## go-pkg-autorelease.yml

Usage example

```yaml
name: AutoRelease

on:
  push:
    branches: [main]
    paths: [VERSION]
  workflow_dispatch:

jobs:
  BuildAndRelease:
    uses: mitoteam/shared-actions/.github/workflows/go-pkg-autorelease.yml@main
    secrets: inherit
    permissions:
      contents: write
    with:
          draft_release: false
```
