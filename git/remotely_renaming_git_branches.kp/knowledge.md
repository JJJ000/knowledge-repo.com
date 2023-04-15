---
title: Changing the names of remote git branches
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To rename a remote branch in Git, use the command `git push <remote\_name> <old\_branch\_name><new\_branch\_name>`.
---

**Contents**

[TOC]

### Renaming Branches Remotely in Git

### Prerequisites
Before you can rename a branch remotely, you must have a remote repository set up.

### Renaming the Branch
1. Open a terminal window and navigate to the local repository.
2. Use the `git push` command to push the branch to the remote repository.
3. Use the `git branch` command to rename the branch, specifying the old and new branch names.
4. Use the `git push` command to push the renamed branch to the remote repository.

### Verifying the Rename
1. Use the `git branch` command to ensure that the branch has been renamed.
2. Use the `git fetch` command to pull the branch from the remote repository.
3. Use the `git branch` command to check that the branch has been renamed in the remote repository.
