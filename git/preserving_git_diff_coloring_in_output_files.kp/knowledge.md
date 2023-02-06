---
title: Save the output of git diff with its original coloring to a file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, it is not possible to preserve the coloring when outputting a git diff to a file.
---

**Contents**

[TOC]

## Option 1

The simplest way to save the colored output of `git diff` is to pipe the output to `less` and then save the output to a file.

```
git diff | less -R > output.txt
```

## Option 2

If you have `git` version 2.9.0 or later, you can use the `--color=always` option to force `git diff` to always output colored diffs.

```
git diff --color=always > output.txt
```

## Option 3

If you have `git` version 2.14.0 or later, you can use the `--no-pager` option to force `git diff` to output to the terminal instead of using a pager.

```
git diff --no-pager > output.txt
```

## Option 4

If you have `git` version 2.15.0 or later, you can use the `--no-pager` and `--color=always` options to force `git diff` to output colored diffs directly to a file.

```
git diff --no-pager --color=always > output.txt
```
