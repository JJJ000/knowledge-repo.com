---
title: Create a new branch and transfer the most recent commit(s) to it using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Create a new branch, then use `git cherry-pick` to move the desired commit(s) to the new branch.
---

**Contents**

[TOC]

### Create a New Branch

1. Checkout the current branch: `git checkout <current-branch>`
2. Create a new branch: `git checkout -b <new-branch>`

### Move the Most Recent Commit

1. Identify the commit to move: `git log`
2. Reset the current branch to the commit before the most recent commit: `git reset --hard <commit-id>`
3. Checkout the new branch: `git checkout <new-branch>`
4. Rebase the new branch to include the most recent commit: `git rebase <current-branch>`

### Push the New Branch

1. Push the new branch to the remote repository: `git push --set-upstream origin <new-branch>`

### Clean Up

1. Checkout the current branch: `git checkout <current-branch>`
2. Delete the new branch locally: `git branch -D <new-branch>`
