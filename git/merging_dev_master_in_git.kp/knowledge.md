---
title: Combine the development branch with the master branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To merge development with master, use the command `git merge development`.
---

**Contents**

[TOC]

### Step 1: Checkout master

Checkout the master branch and pull the latest changes from the remote repository:

`git checkout master`

`git pull origin master`

### Step 2: Merge development branch

Merge the development branch into the master branch:

`git merge development`

### Step 3: Push to remote

Push the changes to the remote repository:

`git push origin master`

### Step 4: Clean up

Delete the development branch:

`git branch -d development`

`git push origin --delete development`
