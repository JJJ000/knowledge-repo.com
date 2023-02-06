---
title: What is the process for selecting specific file extensions when using git diff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `-- `*.<file\_extension>`` option to filter git diff based on file extensions.
---

**Contents**

[TOC]

**Section 1: Installing diff-filter**

1. Install `diff-filter`, a command-line tool for filtering git diffs, using the following command:

```
$ npm install -g diff-filter
```

**Section 2: Running diff-filter**

1. Run `diff-filter` with the `--extensions` flag to filter git diffs based on file extensions. The `--extensions` flag takes a comma-separated list of file extensions. For example, to filter out all files except those with the `.js` and `.html` extensions, run the following command:

```
$ diff-filter --extensions=js,html
```

**Section 3: Output**

1. The output of the command will be a filtered git diff.

**Section 4: Additional Options**

1. `diff-filter` also supports additional flags, such as `--ignore-whitespace`, `--ignore-case`, and `--strip-trailing-cr`. For more information, see the `diff-filter` documentation.
