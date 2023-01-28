---
title: What is the best way to locate significant commits in git history?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git log --stat` to view the commit history and identify large commits based on the number of files and lines changed.
---

**Contents**

[TOC]

### Using Git Log

The easiest way to identify large commits in git history is to use the `git log` command. This command will show a list of all the commits that have been made to the repository, including the size of each commit. By sorting the list by size, you can quickly identify the largest commits.

### Using Git Diff

Another way to identify large commits in git history is to use the `git diff` command. This command will compare two versions of the repository and show the differences between them. By looking at the differences between versions, you can quickly identify any large changes that have been made.

### Using Git Blame

The third way to identify large commits in git history is to use the `git blame` command. This command will show a list of all the commits that have been made to the repository, including the size of each commit. By looking at the size of each commit, you can quickly identify any large commits.

### Using Git Bisect

Finally, you can use the `git bisect` command to identify large commits in git history. This command will allow you to quickly search through the repository's history and identify any large changes that have been made.
