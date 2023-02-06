---
title: Undoing part of a commit using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To revert part of a commit with git, use the `git revert -p` command.
---

**Contents**

[TOC]

### Step 1: Checkout the Commit
To revert part of a commit with git, the first step is to check out the commit. This can be done with the `git checkout` command. 

### Step 2: Create a New Branch
Once the commit has been checked out, the next step is to create a new branch. This can be done with the `git branch` command. The new branch should be created with a descriptive name, such as "revert-part-of-commit".

### Step 3: Revert the Commit
Once the new branch has been created, the next step is to revert the commit. This can be done with the `git revert` command. The revert command should specify the commit to be reverted, as well as the files that should be reverted.

### Step 4: Merge the Reverted Commit
The final step is to merge the reverted commit into the master branch. This can be done with the `git merge` command. The branch containing the reverted commit should be specified as the source branch, and the master branch should be specified as the destination branch.
