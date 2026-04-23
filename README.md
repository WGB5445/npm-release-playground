# npm-release-playground

Playground repository to test guarded npm release workflows.

## Release modes

- Manual dry run: run workflow_dispatch with `dry_run=true`
- Manual publish: run workflow_dispatch with:
  - `dry_run=false`
  - `confirm_publish=publish`
  - `confirm_version=<package.json version>`
- Tag publish: push tag matching version (`v0.1.0-beta.1` or `0.1.0-beta.1`)

## Setup required before real publish

1. Configure npm Trusted Publisher for this repo and `release.yml`
2. Create GitHub Environment `npm-release` with required reviewers
3. Restrict tag creation to release maintainers
