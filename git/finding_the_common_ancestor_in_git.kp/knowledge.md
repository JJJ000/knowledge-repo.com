---
title: Find the shared starting point of two branches in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: The most recent common ancestor of two branches can be found by running the `git merge-base` command.
---

**Contents**

[TOC]

### Using git merge-base

The `git merge-base` command is used to find the most recent common ancestor of two branches. It takes two branch names as arguments and returns the commit SHA of the common ancestor.

### Syntax

The syntax for `git merge-base` is:

```git
git merge-base <branch1> <branch2>
```

### Example

For example, to find the most recent common ancestor of the `master` and `topic` branches, you would run the following command:

```git
git merge-base master topic
```

This command will return the commit SHA of the most recent common ancestor of the two branches.
