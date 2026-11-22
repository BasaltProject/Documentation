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

### Charts

A fenced block tagged `chart` draws horizontal bars. Header lines come first, then `---`, then groups separated by a
blank line: an optional group name and `series: value` lines. A series keeps its colour across groups; `colors:` pins
a series to a palette slot (0 to 7, separated by `;`) so a name has the same colour in every chart.

````mdx
```chart
title: Time per call
note: Less is better.
unit: ns
scale: log
scope: group
colors: Before=0; After=2
---
Region check
Before: 4996
After: 276

Chat
Before: 1486
After: 238
```
````

`scale: log` draws a logarithmic scale and says so in the note, and `scope: group` gives each group its own scale
instead of sharing one. A block that does not parse is shown as plain code.

## License

[MIT](LICENSE).
