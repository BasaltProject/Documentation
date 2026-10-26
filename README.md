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

## Overview

This repository holds the content. The site that renders it lives in
[Website](https://github.com/BasaltProject/Website) and pulls this repository in
as a submodule.

## Layout

```
<section>/<order>-<slug>.mdx
```

`<section>` is a directory and matches a section registered in the site. The
numeric prefix orders pages within a section and is stripped from the URL, so
`server/02-installation.mdx` is served at `/docs/server/installation`.

## Page format

Every page opens with a front matter head:

```mdx
---
title: Installation
description: One sentence, shown under the title and in search results.
---
```

The body is markdown. It can also use components, which is what the `.mdx`
extension is for:

```mdx
<x-docs.callout type="warning" title="Before you start">
Accept the EULA first. The server writes `eula.toml` and stops on first start.
</x-docs.callout>
```

`type` is `note`, `tip` or `warning`. The body of a callout is markdown too.

Fenced code blocks are highlighted. Tag them with a language so they are:
`lua`, `bash`, `toml`.

## Editing

Pages are plain files: edit them here, commit, and the site picks them up on its
next deploy. Adding a page is adding a file. Adding a section needs a matching
entry on the site side.
