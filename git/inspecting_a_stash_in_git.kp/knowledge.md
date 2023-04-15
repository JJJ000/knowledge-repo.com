---
title: Examine the contents of a stash without implementing them
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can view the contents of a stash by using the command `git stash show` without applying it.
---

**Contents**

[TOC]

### git stash show
The `git stash show` command allows users to view the contents of a stash without applying it. This command can be used with a specific stash reference, or without one to show the latest stash.

### git stash list
The `git stash list` command can be used to view a list of stashes and the associated commit messages. This can be used to get an overview of the changes in each stash without applying them.

### git diff
The `git diff` command can be used to view the differences between the current working directory and the contents of a specific stash. This allows users to view the changes in a stash without applying them.

### git show
The `git show` command can be used to view the contents of a stash commit. This allows users to view the full contents of a stash without applying it.
