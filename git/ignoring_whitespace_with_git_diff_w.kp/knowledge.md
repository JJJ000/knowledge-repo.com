---
title: Git diff -w to disregard whitespace only at the beginning and end of lines
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: No, git diff -w ignores whitespace changes throughout the entire line.
---

**Contents**

[TOC]

Yes

### How to Ignore Whitespace at Start & End of Lines

Git provides a `-w` option for the `diff` command that can be used to ignore whitespace at the start and end of lines. This option can be used with the `--ignore-all-space` option to ignore all whitespace differences.

To ignore whitespace at the start and end of lines, use the following command:

```
git diff -w
```

### How to Ignore All Whitespace

Git provides a `--ignore-all-space` option for the `diff` command that can be used to ignore all whitespace differences. This option can be used with the `-w` option to ignore whitespace at the start and end of lines.

To ignore all whitespace, use the following command:

```
git diff --ignore-all-space
```

### Combining Options

The `-w` and `--ignore-all-space` options can be combined to ignore whitespace at the start and end of lines, as well as all other whitespace differences.

To ignore whitespace at the start and end of lines, as well as all other whitespace differences, use the following command:

```
git diff -w --ignore-all-space
```
