---
title: What is the most efficient way to determine if there are any uncommitted changes in a program?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git status` command to programmatically determine if there are uncommitted changes in Git.
---

**Contents**

[TOC]

### Using Git Status

The easiest way to determine if there are uncommitted changes in Git is to use the `git status` command. This command will show the current state of the repository and any changes that have been made, but not yet committed.

### Using Git Diff

Another way to determine if there are uncommitted changes in Git is to use the `git diff` command. This command will show any differences between the current state of the repository and the last committed version. 

### Using Git Log

The final way to determine if there are uncommitted changes in Git is to use the `git log` command. This command will show the list of commits that have been made to the repository. If the last commit does not match the current state of the repository, then there are uncommitted changes.
