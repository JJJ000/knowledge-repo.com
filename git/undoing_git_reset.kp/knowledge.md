---
title: What is the process for reversing a 'git reset' command?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can undo a git reset by using the command `git reset --hard <commit-hash>`.
---

**Contents**

[TOC]

### Using git reflog

1. Run `git reflog` to view a list of all the changes made to the repository.
2. Find the commit that you want to undo the reset on.
3. Copy the hash of the commit you want to undo the reset on.
4. Run `git reset <hash>` to reset the repository to the commit you want.

### Using git revert

1. Run `git log` to view a list of all the changes made to the repository.
2. Find the commit that you want to undo the reset on.
3. Copy the hash of the commit you want to undo the reset on.
4. Run `git revert <hash>` to undo the reset and create a new commit.
