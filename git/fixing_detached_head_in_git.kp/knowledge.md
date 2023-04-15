---
title: How to revert back to a branch from 'detached head' state in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To return from a detached HEAD state, use the command `git checkout <branch-name>`.
---

**Contents**

[TOC]

### Understanding the Detached HEAD State

The detached HEAD state is a state in git where the HEAD pointer is not pointing to a branch, but instead to a commit. This can happen when you check out a commit directly or when you check out a branch that no longer exists. 

### How to Return from Detached HEAD State

The easiest way to return from a detached HEAD state is to checkout a branch. This can be done by running the command `git checkout <branch-name>`. This will return the HEAD pointer to the branch specified. 

### Creating a New Branch

If you don't have a branch that you want to return to, you can create a new branch. To create a new branch, run the command `git checkout -b <branch-name>`. This will create the branch and return the HEAD pointer to the new branch. 

### Stashing Changes

If you have made changes while in the detached HEAD state, you may want to stash them before returning to a branch. To do this, run the command `git stash`. This will store the changes in a temporary stash and allow you to return to a branch without losing your changes.
