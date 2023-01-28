---
title: Can I go back to a previous branch using git checkout?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Yes, you can use the command `git checkout -` to checkout the previous branch.
---

**Contents**

[TOC]

### Git Checkout
Git checkout is a command that allows you to switch between different branches in a repository. It can be used to switch between existing branches, or to create a new branch and switch to it.

### Checking Out Previous Branch
To check out a previous branch, you can use the `git checkout` command with the name of the branch you want to switch to. For example, if you want to switch to a branch named `my-branch`, you can use the command `git checkout my-branch`.

### Checking Out a Previous Commit
In some cases, you may want to switch to a specific commit in the repository's history. To do this, you can use the `git checkout` command with the commit's SHA-1 hash. For example, if you want to switch to a commit with the SHA-1 hash `abc123`, you can use the command `git checkout abc123`.

### Checking Out a Tag
You can also use the `git checkout` command to switch to a specific tag in the repository. To do this, you can use the command `git checkout <tag-name>`. For example, if you want to switch to a tag named `v1.0`, you can use the command `git checkout v1.0`.
