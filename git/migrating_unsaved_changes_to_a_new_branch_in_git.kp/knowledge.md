---
title: Transferring unstaged modifications to a different branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Create a new branch, then use git cherry-pick to move the uncommitted changes to the new branch.
---

**Contents**

[TOC]

### Creating a New Branch
1. In the terminal, type `git checkout -b <new_branch_name>` to create a new branch.
2. Type `git branch` to make sure the new branch is created.

### Staging Changes
1. Type `git add <file_name>` to stage the changes.
2. Type `git status` to make sure the changes are staged.

### Committing Changes
1. Type `git commit -m "<commit_message>"` to commit the changes.
2. Type `git log` to make sure the changes are committed.

### Pushing Changes
1. Type `git push origin <new_branch_name>` to push the changes to the new branch.
2. Type `git branch -a` to make sure the changes are pushed to the new branch.
