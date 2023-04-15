---
title: What are the differences between commits in different branches of git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the `git diff` command to compare the differences between branches.
---

**Contents**

[TOC]

### Using `git diff`

The `git diff` command can be used to see the differences between two branches. This command will compare the branches and display the differences between them.

### Specifying Branches

When using the `git diff` command, you must specify which branches you want to compare. This can be done by using the following syntax:

`git diff <branch1> <branch2>`

### Using `git log`

The `git log` command can also be used to see the differences between two branches. This command will show the commits on each branch and the differences between them.

### Specifying Branches

When using the `git log` command, you must specify which branches you want to compare. This can be done by using the following syntax:

`git log <branch1>..<branch2>`
