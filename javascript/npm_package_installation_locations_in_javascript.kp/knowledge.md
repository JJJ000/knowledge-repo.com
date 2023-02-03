---
title: What location does npm use to install packages?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Npm installs packages in the node\_modules directory in the current working directory.
---

**Contents**

[TOC]

### Local Installation

By default, npm installs packages to the local directory `node_modules`. This directory is created in the current working directory (where the `package.json` is located).

### Global Installation

Packages can also be installed globally. This is done using the `-g` flag. Global packages are installed to the `prefix`/lib/node_modules directory. The `prefix` is usually `/usr/local` on Unix systems, or `%AppData%` on Windows.

### Scoped Packages

Npm also supports scoped packages. These are packages that are installed in a special directory called `@scope`. For example, if you were to install a package called `@myorg/mypackage`, it would be installed to the `node_modules/@myorg/mypackage` directory.
