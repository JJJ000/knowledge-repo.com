---
title: What is the closest ancestor of a git branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the command `git branch -u <parent\_branch\_name>` to find the nearest parent of a Git branch.
---

**Contents**

[TOC]

### Viewing Branches

To find the nearest parent of a Git branch, you must first view the list of branches in your repository. This can be done by running the command `git branch` in your terminal. This will list out all of the branches in your repository, including the current branch that you are currently on.

### Viewing Commit History

Once you have the list of branches, you can view the commit history of each branch by running the command `git log <branch-name>`. This will show the history of commits that have been made to the specified branch, including the parent commit of the branch.

### Finding the Nearest Parent

The nearest parent of a Git branch can be found by looking at the commit history of the branch. The parent of the branch will be the commit that is closest to the top of the commit history.

### Checking Out the Parent Branch

Once you have found the parent commit of the branch, you can check out the parent branch by running the command `git checkout <parent-branch-name>`. This will switch you to the parent branch, allowing you to view and work on the code from the parent commit.
