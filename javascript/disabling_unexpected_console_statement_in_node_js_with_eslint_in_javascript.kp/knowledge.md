---
title: How can I turn off the "unexpected console statement" warning in Node.js using eslint?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To disable the `unexpected console statement` warning in Node.js, add /* eslint-disable no-console */ at the top of the file.
---

**Contents**

[TOC]

# 1. Using ESLint's "no-console" rule

ESLint provides a "no-console" rule that disables all console statements. To enable this rule, add it to your .eslintrc file:

```
{
  "rules": {
    "no-console": "error"
  }
}
```

# 2. Using ESLint's "global" directive

If you need to use console statements in certain files, you can use the "global" directive to disable the "no-console" rule for those files. Add the following line to the top of the file:

```
/* global console */
```

# 3. Using ESLint's "off" directive

If you need to disable the "no-console" rule for a single line, you can use the "off" directive. Add the following line to the top of the line:

```
// eslint-disable-next-line no-console
```

# 4. Using ESLint's "env" option

If you need to disable the "no-console" rule for all files in a certain environment, you can use the "env" option. Add the following line to your .eslintrc file:

```
{
  "env": {
    "node": {
      "no-console": "off"
    }
  }
}
```
