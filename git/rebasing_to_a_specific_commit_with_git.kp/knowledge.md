---
title: How can I use git to change the base of my project to a particular commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To rebase to a specific commit, use the command `git rebase <commit-hash>`.
---

**Contents**

[TOC]

## Step 1: Checkout the Commit
1. Checkout the desired commit by running the command `git checkout <commit-hash>`

## Step 2: Create a New Branch
2. Create a new branch from the commit by running the command `git branch <new-branch-name>`

## Step 3: Rebase
3. Rebase the new branch onto the current branch by running the command `git rebase <current-branch-name>`

## Step 4: Checkout the Current Branch
4. Checkout the current branch by running the command `git checkout <current-branch-name>`
