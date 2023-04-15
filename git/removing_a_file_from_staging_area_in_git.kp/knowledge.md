---
title: How can I undo a git add for a single file in the staging area?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use `git reset <file>` to remove a single file from the staging area.
---

**Contents**

[TOC]

### Using `git reset`
1. Check the status of the repository using `git status` to find the file you want to remove from the staging area.
2. Use `git reset <file>` to unstage the file. 

### Using `git rm`
1. Check the status of the repository using `git status` to find the file you want to remove from the staging area.
2. Use `git rm --cached <file>` to remove the file from the staging area.
