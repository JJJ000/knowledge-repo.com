---
title: What is the method for determining if a branch has already been merged into the master branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can view the commit history of the master branch to see if the branch has been merged into it.
---

**Contents**

[TOC]

### Check Git Log

One way to know if a branch has been already merged into master is to check the Git log. You can use the command `git log` to view the history of commits in the current branch. This will show you all the commits that have been made to the current branch and any branches that have been merged into it.

### Check Merge History

Another way to know if a branch has been already merged into master is to check the merge history. You can use the command `git log --merges` to view the history of merges in the current branch. This will show you all the branches that have been merged into the current branch, including master.

### Check Branches

Finally, you can check the list of branches in your repository to see which branches have been merged into master. You can use the command `git branch --merged` to view the list of branches that have been merged into the current branch. This will show you all the branches that have been merged into the current branch, including master.
