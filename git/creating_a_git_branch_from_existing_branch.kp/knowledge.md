---
title: Create a new branch in git based on another branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To create a branch in Git from another branch, use the command `git checkout -b <new-branch-name> <existing-branch-name>`.
---

**Contents**

[TOC]

### Check Out the Branch

In order to create a branch in Git from another branch, the first step is to check out the branch that you want to create the new branch from. This can be done using the command `git checkout <branch_name>`.

### Create the New Branch

Once you have checked out the branch that you want to create the new branch from, you can use the command `git branch <new_branch_name>` to create the new branch.

### Switch to the New Branch

After creating the new branch, you can switch to it using the command `git checkout <new_branch_name>`. This will make the new branch the active branch.

### Push the New Branch to Remote

Finally, you can push the new branch to the remote repository using the command `git push origin <new_branch_name>`. This will make the new branch available to other developers.
