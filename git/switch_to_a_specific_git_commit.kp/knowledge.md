---
title: Check out a specific git commit in the working copy
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Checkout the specific commit with `git checkout <commit>`.
---

**Contents**

[TOC]

### 1. Checkout Commit

To switch to a specific commit, you can use the `git checkout` command. The syntax for this command is `git checkout <commit>`. This will switch the working copy to the specified commit.

### 2. Unstaged Changes

When switching to a specific commit, any changes that have been made to the working copy will be unstaged. This means that any changes that have been made will not be applied to the commit.

### 3. Create Branch

It is recommended to create a new branch when switching to a specific commit. This will allow you to easily switch back to the original commit if needed. To create a new branch, use the command `git checkout -b <branch-name> <commit>`.

### 4. Reset Working Copy

If you want to reset the working copy to the specified commit, you can use the `git reset` command. The syntax for this command is `git reset --hard <commit>`. This will reset the working copy to the specified commit.
