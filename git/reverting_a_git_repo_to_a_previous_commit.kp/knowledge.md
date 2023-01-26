---
title: What is the procedure for restoring a git repository to a prior commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To revert a Git repository to a previous commit, use the `git reset` command with the `--hard` option.
---

**Contents**

[TOC]

### Step 1: Find the Commit Hash

The first step to reverting a Git repository to a previous commit is to find the commit hash of the commit you wish to revert to. This can be done by running the command `git log` in the terminal. This will show a list of all the commits and their corresponding hashes.

### Step 2: Checkout the Commit

Once you have the commit hash, you can checkout the commit by running the command `git checkout <commit-hash>`. This will switch your repository to the commit you specified.

### Step 3: Create a New Branch

It is important to create a new branch before making any changes. This can be done by running the command `git checkout -b <branch-name>`. This will create a new branch and switch to it.

### Step 4: Push the Changes

Once you have made the necessary changes to the repository, you can push the changes to the remote repository by running the command `git push -u origin <branch-name>`. This will push the changes to the remote repository.
