---
title: What is the process for saving only unstaged changes in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To stash only unstaged changes in Git, use the command `git stash --keep-index`.
---

**Contents**

[TOC]

### Stashing Unstaged Changes

### Step 1: View Unstaged Changes 

To view the changes you’ve made to your working directory that have not yet been staged, use the `git diff` command. This will show you a list of all the changes you’ve made that have not yet been added to the staging area.

### Step 2: Stash the Changes 

Once you’ve identified the changes you want to stash, use the `git stash` command to save them. This will save the changes to a special area called the “stash”, where they can be retrieved later if needed.

### Step 3: Verify Stashed Changes 

To verify that the changes have been successfully stashed, use the `git stash list` command. This will show you a list of all the changes that have been stashed.

### Step 4: Retrieve Stashed Changes 

If you need to retrieve the stashed changes, use the `git stash apply` command. This will apply the changes from the stash to your working directory.
