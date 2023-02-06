---
title: Combining two branches in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To merge two branches together in Git, use the command `git merge <branch1> <branch2>`.
---

**Contents**

[TOC]

## Step 1: Checkout the Target Branch
The first step to merging two branches in Git is to check out the target branch. This is the branch that you want to merge your changes into. To do this, use the command:

`git checkout <target_branch>`

## Step 2: Merge the Source Branch
Once you have checked out the target branch, you can merge the source branch into the target branch. To do this, use the command:

`git merge <source_branch>`

## Step 3: Resolve Conflicts
After merging the source branch into the target branch, you may encounter conflicts. If this happens, you will need to resolve the conflicts manually. This can be done by opening the files with conflicts and manually editing them to resolve the conflicts.

## Step 4: Commit the Changes
Once you have resolved all of the conflicts, you can commit the changes to the target branch. To do this, use the command:

`git commit -m "Merged <source_branch> into <target_branch>"`
