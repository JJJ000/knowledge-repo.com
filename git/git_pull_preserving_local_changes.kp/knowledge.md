---
title: Git fetch and merge while preserving local modifications
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git stash` command to save your local changes, then pull, and then apply the stash to restore the local changes.
---

**Contents**

[TOC]

## Git Stash
Git stash allows you to save your local changes and revert back to the most recent commit. This is useful when you need to pull changes from a remote repository without losing your local changes. To use git stash, you first need to add your changes to the stash by running the command `git stash`. This will save all of your local changes to the stash.

## Git Pull
Once your changes have been stashed, you can then run `git pull` to pull down the latest changes from the remote repository. This will update your local repository with the latest changes from the remote repository.

## Git Stash Pop
Once you have pulled the latest changes from the remote repository, you can then run `git stash pop` to apply your local changes back onto the repository. This will apply all of the changes that you previously stashed back onto the repository.

## Git Push
Finally, you can then push your changes back to the remote repository with `git push`. This will update the remote repository with all of the changes that you have made.
