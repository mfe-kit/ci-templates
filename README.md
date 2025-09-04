# MFE-KIT GitHub Actions Pipelines

Repository with shared pipeline templates for GitHub Actions in MFE-KIT.

## Usage

To use a pipeline template from this repository, reference it in your GitHub Actions workflow:

```yaml

name: Build & Release

on:
  push:
    branches: [main]

jobs:
  release:
    uses: mfe-kit/ci-templates/.github/workflows/release.yml@main
    with:
      repo_name: REPO_NAME
    secrets:
      RELEASE_TOKEN: ${{ secrets.RELEASE_TOKEN }}

```
