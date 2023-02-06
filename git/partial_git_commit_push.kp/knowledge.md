---
title: What is the process for selectively pushing certain commits from your local git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git cherry-pick` command to push only some of your local git commits.
---

**Contents**

[TOC]

## Using `git cherry-pick` 
1. Create a list of commits to be pushed. For example, `git log --oneline` can be used to see a list of commits and their hashes. 
2. Use `git cherry-pick` to apply the commits to the current branch. For example, `git cherry-pick <commit hash>`.
3. Push the commits to the remote repository.

## Using `git rebase` 
1. Checkout the branch where the commits need to be pushed.
2. Use `git rebase` to apply the commits to the current branch. For example, `git rebase -i <commit hash>`.
3. Push the commits to the remote repository.
