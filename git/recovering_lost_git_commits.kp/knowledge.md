---
title: What steps do I need to take to retrieve a commit that has been lost in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git reflog` to find the commit, then use `git cherry-pick` to recover it.
---

**Contents**

[TOC]

### Check the reflog

The first and most important step to recovering a lost commit is to check the reflog. The reflog is a log of all the changes to the local repository. It contains all the commits that have been made, even if they have been deleted. To view the reflog, use the command `git reflog`.

### Find the commit

Once you have accessed the reflog, you can search for the commit you are looking for. The reflog will show the SHA-1 hash of the commit, as well as the date and time it was made. Once you have identified the commit, you can use the command `git checkout <SHA-1 hash>` to restore the commit.

### Checkout the commit

Once you have identified the commit, you can use the command `git checkout <SHA-1 hash>` to restore the commit. This will create a new branch with the commit as its HEAD. You can then use the command `git checkout <branch name>` to checkout the new branch and view the commit.

### Rebase the commit

Once you have checked out the commit, you can use the command `git rebase -i <SHA-1 hash>` to move the commit back to its original location in the repository. This will allow you to restore the commit to its original location in the repository.
