---
title: Compare the changes between commits
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To view the differences between commits in Git, use the git diff command.
---

**Contents**

[TOC]

### git diff

The `git diff` command is used to show changes between commits, commit and working tree, etc. It can be used to view the difference between the current working tree and the last commit, the difference between two commits, and the difference between two files.

### Syntax

The syntax for `git diff` is as follows:

`git diff [<options>] [<commit>] [--] [<path>...]`

### Examples

To view the changes between the working tree and the last commit:

`git diff`

To view the changes between two commits:

`git diff <commit1> <commit2>`

To view the changes between two files:

`git diff <file1> <file2>`
