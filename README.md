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
    with:
      draft_release: false # publish it if everything goes well
    secrets: inherit
    permissions:
      contents: write
```

## go-build-and-test.yml

Usage example

```yaml
name: Build-and-Test

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]
  workflow_dispatch:

jobs:
  BuildAndTest:
    uses: mitoteam/shared-actions/.github/workflows/goapp-build-and-test.yml@main
    secrets: inherit
    permissions:
      contents: write
```

## goapp-autorelease.yml

Usage example

```yaml
name: AutoRelease

on:
  push:
    branches: [main]
    paths: [VERSION]
  workflow_dispatch:

jobs:
  AutoRelease:
    uses: mitoteam/shared-actions/.github/workflows/goapp-autorelease.yml@main
    with:
      dist_name: "mt-checklist"
      draft_release: true # do not auto-publish
    secrets: inherit
    permissions:
      contents: write
```
