---
title: Revert the first two commits in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To squash the first two commits in Git, use the command `git rebase -i HEAD~2`.
---

**Contents**

[TOC]

#1 Using `git rebase`

1. Checkout the branch you want to squash commits on: `git checkout <branch_name>`
2. Rebase the branch to the commit before the first commit you want to squash: `git rebase -i <commit_hash>`
3. In the interactive rebase window, change the pick of the first two commits to squash: `s`
4. Save and close the window.

#2 Using `git reset`

1. Checkout the branch you want to squash commits on: `git checkout <branch_name>`
2. Reset the branch to the commit before the first commit you want to squash: `git reset --soft <commit_hash>`
3. Add all changes to the index: `git add -A`
4. Create a new commit with the changes: `git commit -m "Squashed commits"`
