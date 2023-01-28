---
title: What is the best way to remove a large number of files from the staging area without deleting their contents?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To unstage large number of files without deleting the content in Git, use the command `git reset HEAD <file>`.
---

**Contents**

[TOC]

### Using `git reset`

The `git reset` command can be used to unstage a large number of files without deleting the content.

### Syntax

The syntax for the `git reset` command is as follows:

`git reset [<file>...]`

### Usage

To unstage a large number of files, the command should be used with the `--mixed` option. This will unstage the files without deleting the content.

### Example

For example, to unstage all files in the current directory, the following command can be used:

`git reset --mixed .`
