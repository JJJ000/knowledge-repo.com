---
title: Combine the changes from two local branches in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To merge two local branches, use the command `git merge <branch-name>`.
---

**Contents**

[TOC]

## Step 1: Checkout the branch you want to merge into

First you will need to checkout the branch you want to merge into. This is the branch that will contain the changes from the other branch.

You can do this with the following command:

`git checkout <branch-name>`

## Step 2: Merge the other branch into the current branch

Once you are in the branch you want to merge into, you can merge the other branch with the following command:

`git merge <other-branch-name>`

## Step 3: Resolve any conflicts

If there are any conflicts between the two branches, you will need to resolve them manually. This can be done by editing the conflicting files and then adding them to the staging area with the following command:

`git add <filename>`

## Step 4: Commit the merge

Once you have resolved any conflicts, you can commit the merge with the following command:

`git commit -m "Merge <other-branch-name> into <branch-name>"`
