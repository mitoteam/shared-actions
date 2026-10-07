# MiTo Team shared actions

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
