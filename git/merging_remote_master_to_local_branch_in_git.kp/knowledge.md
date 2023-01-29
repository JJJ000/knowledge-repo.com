---
title: How to combine a remote master branch with a local branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git pull origin master` to merge the remote master branch into your local branch.
---

**Contents**

[TOC]

### Create a Local Branch
1. Run `git checkout -b <branch_name>` to create a local branch.

### Fetch and Merge Remote Master
1. Run `git fetch origin` to fetch the remote master.
2. Run `git merge origin/master` to merge the remote master into the local branch.

### Push Local Branch
1. Run `git push origin <branch_name>` to push the local branch to the remote repository.

### Cleanup
1. Run `git branch -d <branch_name>` to delete the local branch.
