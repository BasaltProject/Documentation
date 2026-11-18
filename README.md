<p align="center">
  <a href="https://raw.githubusercontent.com/BasaltProject/.github/main/assets/basalt-logo-white.svg#gh-dark-mode-only">
    <img src="https://raw.githubusercontent.com/BasaltProject/.github/main/assets/basalt-logo-white.svg" alt="Basalt" width="360">
  </a>
  <a href="https://raw.githubusercontent.com/BasaltProject/.github/main/assets/basalt-logo-black.svg#gh-light-mode-only">
    <img src="https://raw.githubusercontent.com/BasaltProject/.github/main/assets/basalt-logo-black.svg" alt="Basalt" width="360">
  </a>
</p>

<h2 align="center">Basalt Documentation</h2>

<p align="center">
  <strong>The documentation published at <a href="https://basaltmc.org/docs">basaltmc.org/docs</a>.</strong>
</p>

<p align="center">
  <img alt="Format" src="https://img.shields.io/badge/format-MDX-1B1F24?logo=mdx&logoColor=white">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-green">
</p>

## About

This repository holds the content. The site that renders it lives in [Website](https://github.com/BasaltProject/Website),
which pulls this repository in as a submodule. Pages are plain files: edit them here, commit, and the site picks them
up on its next deploy.

## Pages

Each page is `<section>/<order>-<slug>.mdx`. The numeric prefix orders pages and is dropped from the URL, so
`server/02-installation.mdx` is served at `/docs/server/installation`. A new section needs a matching entry on the
site side.

```mdx
---
title: Installation
description: One sentence, shown under the title and in search results.
group: Configuration
---
```

The body is markdown, with callouts (`<x-docs.callout type="note|tip|warning" title="...">`) and fenced code blocks
tagged with a language (`lua`, `bash`, `toml`).

## License

[MIT](LICENSE).
