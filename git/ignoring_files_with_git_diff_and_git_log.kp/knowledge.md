---
title: How can I make git-diff and git log ignore newly added and deleted files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git diff and git log can be configured to ignore new and deleted files using the `--diff-filter=ACMRTUXB` flag.
---

**Contents**

[TOC]

1. Using `git diff`
  - Use the `--no-renames` flag to tell `git diff` to ignore changes in the number of files.
  - Use the `--name-only` flag to tell `git diff` to show only the names of the files that have changed.
  - Use the `--diff-filter` flag to tell `git diff` to only show changes for certain types of files. For example, `--diff-filter=ACD` will show only added, copied, and deleted files.

2. Using `git log`
  - Use the `--name-only` flag to tell `git log` to show only the names of the files that have changed.
  - Use the `--diff-filter` flag to tell `git log` to only show changes for certain types of files. For example, `--diff-filter=ACD` will show only added, copied, and deleted files.
  - Use the `--no-renames` flag to tell `git log` to ignore changes in the number of files.
