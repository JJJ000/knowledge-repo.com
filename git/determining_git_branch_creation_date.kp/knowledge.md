---
title: What is the method for finding out when a git branch was created?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The date a Git branch was created can be determined by running the command `git log --oneline --decorate --graph --all`.
---

**Contents**

[TOC]

### Using `git log`

The `git log` command can be used to view the history of a particular branch. To view the creation date of a branch, use the `--date-order` flag. This will display the commits in the branch in chronological order, with the first commit being the branch's creation.

### Using `git branch`

The `git branch` command can also be used to view the creation date of a branch. The `-v` flag will display the date of the last commit on each branch. The branch with the oldest last commit is the branch that was created first.

### Using `git show-branch`

The `git show-branch` command can also be used to view the creation date of a branch. This command will display the commits in the branch in chronological order, with the first commit being the branch's creation.

### Using `git reflog`

The `git reflog` command can be used to view the history of a particular branch. This command will display the date and time of each commit in the branch. The first commit in the reflog will be the branch's creation.
