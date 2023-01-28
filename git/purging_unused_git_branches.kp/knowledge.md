---
title: Purging obsolete git branches from a remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git remote prune origin` to delete any remote branches that no longer exist in the upstream repository.
---

**Contents**

[TOC]

### Removing Branches Locally
1. Check the list of local branches: `git branch`
2. Delete the branch: `git branch -d <branch_name>`

### Removing Branches Remotely
1. Check the list of remote branches: `git branch -r`
2. Delete the branch: `git push origin --delete <branch_name>`
