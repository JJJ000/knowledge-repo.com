---
title: Determine which remote branch a local branch is linked to
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To find out which remote branch a local branch is tracking in Git, use the command `git branch -vv`.
---

**Contents**

[TOC]

### 1. Check Tracking Information

To check which remote branch a local branch is tracking, use the `git branch -vv` command. This command will list all of the local branches and their associated upstream branches.

### 2. Identify the Local Branch

Identify the local branch you want to check. This can be done by running `git branch` to list all of the local branches.

### 3. Check Tracking Information

Once you have identified the local branch, run `git branch -vv` to get the tracking information. This command will return the name of the remote branch that the local branch is tracking.

### 4. Confirm Tracking Information

Finally, you can confirm that the local branch is tracking the correct remote branch by running `git status`. This will show the current branch and the remote branch it is tracking.
