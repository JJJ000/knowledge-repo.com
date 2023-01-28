---
title: What is the process for copying the contents of one local branch to a new local branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the command `git checkout -b <new\_branch> <source\_branch>` to copy the content of a branch to a new local branch in Git.
---

**Contents**

[TOC]

### Step 1: Create a New Local Branch

1. Run `git checkout -b <new-branch-name>` to create a new local branch. 

### Step 2: Checkout the Desired Branch

1. Run `git checkout <desired-branch>` to switch to the desired branch.

### Step 3: Merge the Desired Branch into the New Branch

1. Run `git merge <desired-branch>` to merge the desired branch into the new branch.

### Step 4: Push the New Branch to Remote

1. Run `git push origin <new-branch-name>` to push the new branch to remote.
