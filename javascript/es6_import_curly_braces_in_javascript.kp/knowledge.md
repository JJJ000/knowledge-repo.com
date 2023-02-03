---
title: What are the circumstances for using curly braces when importing in es6?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Curly braces should be used when importing a specific method or property from a module in ES6.
---

**Contents**

[TOC]

### When importing a single export

When importing a single export, you can use the following syntax:

`import { exportName } from 'module-name';`

### When importing multiple exports

When importing multiple exports, you can use the following syntax:

`import { export1, export2, ..., exportN } from 'module-name';`

### When importing an entire module

When importing an entire module, you can use the following syntax:

`import * as moduleName from 'module-name';`

### When renaming an imported module

When renaming an imported module, you can use the following syntax:

`import { exportName as aliasName } from 'module-name';`
