---
title: What is the distinction between "git add -A" and "git add ."?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: `git add -A` stages all changes, including deletions, while `git add .` stages all changes, excluding deletions.
---

**Contents**

[TOC]

### git add -A

`git add -A` is a shorthand command for adding all changes in the current directory, including new files, modified files, and deleted files. It is the equivalent of running `git add .` followed by `git add -u`.

### git add .

`git add .` adds all new and modified files in the current directory to the staging area. It does not add deleted files to the staging area.

### Differences

The primary difference between `git add -A` and `git add .` is that `git add -A` adds both new and modified files, as well as deleted files, to the staging area, while `git add .` only adds new and modified files.
