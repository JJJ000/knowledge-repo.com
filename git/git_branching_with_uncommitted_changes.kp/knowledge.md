---
title: Creating a new branch in git and transferring any uncommitted changes from the master branch to it
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a new branch from the current Master branch and push the uncommitted changes to the new branch.
---

**Contents**

[TOC]

# Step 1: Create a New Branch

1. Open the Git command line.
2. Enter `git branch <new-branch-name>` to create a new branch.
3. Enter `git checkout <new-branch-name>` to switch to the new branch.

# Step 2: Add Uncommitted Changes to the New Branch

1. Enter `git add .` to add all modified and untracked files to the staging area.
2. Enter `git commit -m "<commit-message>"` to commit the changes to the new branch.

# Step 3: Push the New Branch to Remote

1. Enter `git push --set-upstream origin <new-branch-name>` to push the new branch to the remote repository.

# Step 4: Checkout Master Branch

1. Enter `git checkout master` to switch back to the master branch.
