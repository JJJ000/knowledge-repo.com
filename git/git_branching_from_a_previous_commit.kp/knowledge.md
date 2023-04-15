---
title: Create a new branch from a previous commit in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To create a new branch from a previous commit using Git, use the `git checkout -b <new\_branch\_name> <commit\_sha>` command.
---

**Contents**

[TOC]

### Step 1: Find Previous Commit

To find the previous commit, use the `git log` command. This command will list all commits in reverse chronological order.

### Step 2: Checkout the Commit

Once you have found the desired commit, use the `git checkout` command to switch to the commit. This command will create a new branch that points to the commit.

### Step 3: Create New Branch

To create a new branch from the commit, use the `git branch` command. This will create a new branch from the commit.

### Step 4: Push the Branch

Finally, to push the new branch to the remote repository, use the `git push` command. This will push the new branch to the remote repository.
