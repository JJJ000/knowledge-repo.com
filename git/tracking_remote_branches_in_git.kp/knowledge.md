---
title: Which remote/upstream branches are being tracked by my git branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the command `git branch -vv` to see which local branches are tracking which remote branches.
---

**Contents**

[TOC]

### Viewing Remote Tracking Branches

To view the remote tracking branches for a given repository, use the `git branch -vv` command. This will list all local branches and their associated upstream branches.

### Identifying Tracking Branches

The output of the `git branch -vv` command will list all local branches and their associated upstream branches. The upstream branch will be indicated by a `[<remote>/<branch>]` entry after the name of the local branch.

For example, if the output of the command is `master [origin/master] abc123`, this indicates that the local branch `master` is tracking the remote branch `origin/master`.

### Viewing Remote Branches

To view all the remote branches for a given repository, use the `git branch -r` command. This will list all remote branches and their associated URLs.

### Viewing Remote Branches in Detail

To view more detailed information about a remote branch, use the `git show-branch` command. This will show the commit history of the remote branch and its associated upstream branches.
