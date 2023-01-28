---
title: What is the best way to view the contents of a stash in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git stash show` command to preview the contents of a stash.
---

**Contents**

[TOC]

### Overview

Git Stash is a feature of Git that allows you to store uncommitted changes in a temporary area, so that you can switch branches without losing your work. Stashing is a useful way to save changes that you do not want to commit yet, but do not want to discard either. It is also useful for quickly switching between branches without having to commit your changes.

### How to Preview Stash Contents

Git provides a command to preview the contents of your stash. This command is `git stash show`, and it will show you the list of changes that have been stashed. It will also show the details of each change, such as the files that have been modified and the lines that have been added or removed. 

### Options

The `git stash show` command also accepts a few options that can be used to customize the output. For example, the `--stat` option will show you the number of lines that have been added or removed from each file. The `--patch` option will show you the actual changes in each file, and the `-p` option will show you the changes in a more detailed format.

### Conclusion

The `git stash show` command is a useful way to preview the contents of your stash, and it can be used to view the changes that have been stashed. It also accepts a few options that can be used to customize the output, such as the `--stat` and `--patch` options.
