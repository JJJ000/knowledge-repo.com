---
title: What is the process for retrieving changes from another branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To get changes from another branch in Git, use the `git pull` command.
---

**Contents**

[TOC]

## 1. Fetch

The first step to getting changes from another branch is to fetch the remote branch. This can be done by running the command `git fetch <remote> <branch>`, where `<remote>` is the name of the remote and `<branch>` is the name of the branch.

## 2. Checkout

Once the remote branch has been fetched, the next step is to checkout the branch. This can be done by running the command `git checkout <branch>`, where `<branch>` is the name of the branch.

## 3. Merge

The final step is to merge the changes from the remote branch into the current branch. This can be done by running the command `git merge <branch>`, where `<branch>` is the name of the branch.
