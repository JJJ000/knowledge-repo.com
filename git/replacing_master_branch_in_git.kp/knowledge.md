---
title: What is the process for completely replacing the master branch in git with the contents of another branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Checkout the desired branch, then run `git branch -f master <branch\_name>` to replace the master branch with the desired branch.
---

**Contents**

[TOC]

### 1. Create a New Branch

Create a new branch from the branch you want to use as the new master branch:

`git checkout -b new-master`

### 2. Switch to the New Branch

Switch to the new branch:

`git checkout new-master`

### 3. Push the New Branch

Push the new branch to the remote repository:

`git push origin new-master`

### 4. Set the New Branch as the Default

Set the new branch as the default branch:

`git branch -m master new-master`

`git push origin --delete master`

`git push origin -u new-master`
