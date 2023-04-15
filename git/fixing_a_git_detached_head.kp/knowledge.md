---
title: What is the procedure for resolving a git detached head issue?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Checkout a branch (e.g. master) to re-attach the head to a branch.
---

**Contents**

[TOC]

### 1. Check Out the Detached Head

To fix a detached head, the first step is to check out the detached head. This can be done by using the `git checkout` command followed by the commit ID of the detached head. This will switch the current branch to the detached head.

### 2. Create a New Branch

Once the detached head is checked out, it is recommended to create a new branch from the detached head. This can be done by using the `git branch` command followed by the name of the new branch. This will create a new branch from the detached head which will keep the detached head safe.

### 3. Rebase the New Branch

After creating the new branch, it is recommended to rebase the new branch. This can be done by using the `git rebase` command followed by the name of the branch that the new branch should be rebased onto. This will ensure that the new branch is up-to-date with the original branch.

### 4. Merge the New Branch

Once the new branch is rebased, it is recommended to merge the new branch into the original branch. This can be done by using the `git merge` command followed by the name of the new branch. This will ensure that the changes from the detached head are merged into the original branch.
