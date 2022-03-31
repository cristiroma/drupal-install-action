# Install dependencies on a Drupal 8+ project

## Usage

```yml
on: [pull_request]
name: Test 
jobs:
  qa:
    runs-on: ubuntu-latest
    steps:

      - uses: cristiroma/drupal-install-action@main
        with:
          dev: true
```

## Environment

- `GITHUB_SHA` - It uses this environment variable to compute an artifact filename based on first 7 characters from SHA.

## Inputs

- `dev` - (Default: `false`) - When `true` it installs all composer dependencies (including development). This is useful when creating a release to run tests.
