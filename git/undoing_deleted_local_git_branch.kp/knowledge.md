---
title: Revert the deletion of a local branch in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To undo a local branch delete, use the command `git branch <branchname>` to restore the deleted branch.
---

**Contents**

[TOC]

### Check the Local Branches

Run the following command in the terminal to check the local branches:

`git branch`

### Restore Deleted Branch

If the deleted branch is still present in the list of local branches, then it can be restored by running the following command:

`git branch <branch_name>`

### Check Remote Branches

If the deleted branch is not present in the list of local branches, then it can be checked in the remote branches by running the following command:

`git branch -r`

### Restore Deleted Remote Branch

If the deleted branch is present in the list of remote branches, then it can be restored by running the following command:

`git checkout -b <branch_name> origin/<branch_name>`
