---
title: Pull changes from the master branch into other git branches
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To update Git branches from master, use the `git pull` command.
---

**Contents**

[TOC]

### Update Local Branches

1. Checkout the branch you want to update: `git checkout <branch-name>`
2. Fetch the latest changes from the master branch: `git fetch origin master`
3. Merge the latest changes from the master branch into your branch: `git merge origin/master`

### Update Remote Branches

1. Push the latest changes from your local branch to the remote branch: `git push origin <branch-name>`
2. Fetch the latest changes from the remote branch: `git fetch origin <branch-name>`
3. Merge the latest changes from the remote branch into your local branch: `git merge origin/<branch-name>`

### Resolve Conflicts

1. Check for conflicts: `git status`
2. Open the conflicted files and resolve the conflicts
3. Commit the resolved changes: `git commit -m "Resolved conflicts"`

### Push Changes

1. Push the changes to the remote branch: `git push origin <branch-name>`
