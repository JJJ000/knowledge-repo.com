---
title: What is the distinction between using git checkout --track origin/branch and git checkout -b branch origin/branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git checkout --track origin/branch creates a local branch that tracks the remote branch, while git checkout -b branch origin/branch creates a new local branch and sets it to track the remote branch.
---

**Contents**

[TOC]

### Git Checkout --track Origin/Branch

Git checkout --track origin/branch is used to create a local branch that tracks a remote branch. This command creates a local branch with the same name as the remote branch, and the local branch is configured to track the remote branch. 

### Git Checkout -b Branch Origin/Branch

Git checkout -b branch origin/branch is used to create a new local branch that is based off of a remote branch. This command creates a new local branch with the specified name, and sets the local branch to track the remote branch. Unlike git checkout --track origin/branch, this command does not require the local and remote branches to have the same name.
