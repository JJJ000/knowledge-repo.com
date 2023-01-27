---
title: Resetting a single file to its original state
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: A hard reset of a single file in Git can be done by running `git checkout -- <file>`.
---

**Contents**

[TOC]

### Find the File
1. Navigate to the repository containing the file.
2. Use the `git status` command to find the file.

### Unstage the File
1. Use the `git reset HEAD <file>` command to unstage the file.

### Discard Changes
1. Use the `git checkout -- <file>` command to discard any changes made to the file.

### Commit the Changes
1. Use the `git commit -m "<message>"` command to commit the changes.
