---
title: What is the procedure for obtaining a branch using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To download a branch with git, use the command `git checkout <branch-name>`.
---

**Contents**

[TOC]

### Downloading a Branch with Git

### Step 1: Fetch the Remote Branch

Run the command `git fetch <remote_name> <branch_name>` to fetch the remote branch.

### Step 2: Checkout the Remote Branch

Run the command `git checkout -b <local_branch_name> <remote_name>/<branch_name>` to checkout the remote branch.

### Step 3: Merge the Remote Branch

Run the command `git merge <remote_name>/<branch_name>` to merge the remote branch into your local branch.

### Step 4: Push the Local Branch

Run the command `git push <remote_name> <local_branch_name>` to push the local branch to the remote repository.
