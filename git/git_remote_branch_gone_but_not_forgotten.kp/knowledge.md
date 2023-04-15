---
title: Although the git remote branch was deleted, it is still showing up when running the 'branch -a' command
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The branch still appears in `branch -a` because it is cached locally.
---

**Contents**

[TOC]

### What Happened
When a Git remote branch is deleted, it will still appear when running the command `git branch -a` even though it has been removed. This is because the `git branch -a` command shows all the branches, both local and remote.

### Why Does it Appear
When a remote branch is deleted, the local references to it are not removed. This means that when running `git branch -a`, the deleted remote branch will still appear in the list.

### How to Remove It
To remove the deleted remote branch from the list, you will need to run the command `git remote prune origin`. This will remove all the references to the deleted remote branch from the local repository.

### Conclusion
When a Git remote branch is deleted, it will still appear when running the command `git branch -a`. To remove the deleted remote branch from the list, you will need to run the command `git remote prune origin`.
