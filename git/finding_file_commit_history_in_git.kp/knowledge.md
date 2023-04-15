---
title: What is the commit that introduced a particular file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git log -- <filename>` to find the commit in which a given file was added in Git.
---

**Contents**

[TOC]

### Check File History

The easiest way to find the commit in which a given file was added in Git is to check the file's history. This can be done by running the command `git log --follow <filename>`. This will show the commits that have modified the file, including the one that added it.

### Check Commit History

Another way to find the commit in which a given file was added in Git is to check the commit history. This can be done by running the command `git log -- <filename>`. This will show the commits that have modified the file, including the one that added it.

### Check Blame

A third way to find the commit in which a given file was added in Git is to check the blame. This can be done by running the command `git blame <filename>`. This will show the commits that have modified the file, including the one that added it.

### Check Diff

A fourth way to find the commit in which a given file was added in Git is to check the diff. This can be done by running the command `git diff <commit> <filename>`. This will show the changes that were made in the commit, including the addition of the file.
