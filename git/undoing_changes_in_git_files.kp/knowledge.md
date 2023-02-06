---
title: Revert the changes made to certain files using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To undo changes in some files, use the `git checkout` command.
---

**Contents**

[TOC]

#1 Reset to a Specific Commit

1. Use `git log` to find the commit you want to reset to.
2. Use `git reset --hard <commit-hash>` to reset to the specific commit.

#2 Revert to a Specific Commit

1. Use `git log` to find the commit you want to revert to.
2. Use `git revert <commit-hash>` to revert to the specific commit.

#3 Undo Changes to a Single File

1. Use `git checkout -- <file-name>` to undo changes to a single file.

#4 Undo Changes to Multiple Files

1. Use `git checkout -- <file-name1> <file-name2>` to undo changes to multiple files.
