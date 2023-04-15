---
title: How can I replace a branch on another branch in git, instead of combining them?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To overwrite a branch on another branch in Git, you can use the `git reset --hard` command.
---

**Contents**

[TOC]

### 1. Create a New Branch

The first step is to create a new branch off of the branch that you want to overwrite. This can be done by running the command `git checkout -b <new_branch_name> <source_branch>`. This will create a new branch with the name `<new_branch_name>` that is based off of the `<source_branch>`.

### 2. Reset the Source Branch

The next step is to reset the source branch to the state that you want it to be in. This can be done by running the command `git reset --hard <commit_hash>` where `<commit_hash>` is the hash of the commit that you want the source branch to be reset to.

### 3. Merge the New Branch

Once the source branch has been reset, the new branch can be merged into it. This can be done by running the command `git merge <new_branch_name>`. This will merge the new branch into the source branch and any changes that were made in the new branch will be applied to the source branch.

### 4. Clean Up

The last step is to clean up any unnecessary branches. This can be done by running the command `git branch -d <new_branch_name>`. This will delete the new branch that was created and the source branch will now be in the state that was desired.
