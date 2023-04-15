---
title: How can I relocate specific commits to be based on a different branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use `git cherry-pick` to move certain commits to be based on another branch.
---

**Contents**

[TOC]

### Create a New Branch

1. Checkout the branch you want to base your new branch off of: `git checkout <branch-name>`

2. Create a new branch: `git checkout -b <new-branch-name>`

### Cherry Pick Commits

1. Find the commit you want to move: `git log`

2. Cherry pick the commit: `git cherry-pick <commit-hash>`

3. Repeat for each commit you want to move.

### Push Changes

1. Push the changes to the new branch: `git push origin <new-branch-name>`

### Merge Changes

1. Checkout the branch you want to merge the changes into: `git checkout <branch-name>`

2. Merge the new branch into the current branch: `git merge <new-branch-name>`
