# AMO-brandon/puppeteer-container-headless
> A GitHub Action / Docker image for Puppeteer, the Headless Chrome Node API

## Forked and Updated

This was forked and updated. As the old repo is no longer supported and had some library issues.

## Usage

As a [GitHub Action][actionsUrl]:

```yml
name: CI
on:
  push:
    branches:
      - master
  pull_request:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Install
        # NOTE: this pins the action to a specific commit sha for security
        # reasons but you can also use a version tag if desired. For example:
        # ianwalter/puppeteer-container@v0.2.0
        uses: AMO-brandon/puppeteer-container-test
        with:
          args: pnpm i
      - name: Test
        uses: AMO-brandon/puppeteer-container-test@v0.2.0
        with:
          args: pnpm t
```

## License

Apache 2.0 with Commons Clause - See [LICENSE][licenseUrl]

&nbsp;

Created by [Ian Walter](https://ianwalter.dev)

[buildkiteUrl]: https://github.com/buildkite/docker-puppeteer
[troubleshootingUrl]: https://github.com/GoogleChrome/puppeteer/blob/main/docs/troubleshooting.md
[actionsUrl]: https://github.com/features/actions
[licenseUrl]: https://github.com/ianwalter/puppeteer-container/blob/master/LICENSE
