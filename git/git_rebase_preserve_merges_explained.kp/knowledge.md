---
title: What purpose does the command "git rebase --preserve-merges" serve, and why is it useful?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git`s `rebase --preserve-merges` allows you to combine multiple commits into one, while preserving the original merge commits, allowing you to keep the history of the project intact.
---

**Contents**

[TOC]

### What is Rebase
Rebase is a Git command that allows users to move or combine a sequence of commits to a new base commit. Rebase is often used to integrate changes from one branch into another.

### What is --preserve-merges
The `--preserve-merges` option is a flag that can be used with the `git rebase` command. This flag tells Git to try to recreate merges that were previously made in the history of the branch being rebased.

### Why Use --preserve-merges
Using the `--preserve-merges` option when rebasing can be useful in a few different scenarios. First, it can be used to ensure that any merges that have been made in the branch being rebased are not lost during the rebase process. Second, it can be used to ensure that the commit history is preserved and that any merges that have been made are visible in the commit history.

### How it Works
When the `--preserve-merges` flag is used with the `git rebase` command, Git will attempt to recreate any merges that were previously made in the branch being rebased. This is done by looking for merge commits in the history of the branch being rebased and then attempting to recreate them with the new commits that are being rebased onto the branch. If Git is successful in recreating the merge, then the original merge commit will be replaced with the new merge commit.
