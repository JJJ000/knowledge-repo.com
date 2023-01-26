---
title: How to change an existing local git branch to track a remote branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To make an existing Git branch track a remote branch, use the command `git branch --set-upstream-to <remote>/<branch>`.
---

**Contents**

[TOC]

### Find the Remote Branch

1. Open up the terminal.
2. Type in `git remote -v` to list all the remote branches associated with your local repository. 
3. Find the branch you want to track, and note its name.

### Create a Local Branch

1. Type in `git checkout -b <local-branch-name>` to create a new local branch.
2. Replace `<local-branch-name>` with the name of the local branch you want to create.

### Set Up Tracking

1. Type in `git branch --set-upstream-to=origin/<remote-branch-name> <local-branch-name>`. 
2. Replace `<remote-branch-name>` with the name of the remote branch you noted in Section 1. 
3. Replace `<local-branch-name>` with the name of the local branch you created in Section 2.

### Verify Tracking

1. Type in `git branch -vv` to list all the local branches associated with your repository. 
2. Check that the branch you created in Section 2 is tracking the branch you noted in Section 1.
