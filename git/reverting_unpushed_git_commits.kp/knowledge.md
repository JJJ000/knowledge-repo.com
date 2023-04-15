---
title: How can I undo the last unpushed git commit without losing the changes?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use `git reset --soft HEAD~1` to un-commit the last un-pushed git commit without losing the changes.
---

**Contents**

[TOC]

### Checkout the Commit
1. Use `git log` to view the list of commits
2. Copy the commit hash of the commit you want to un-commit
3. Use `git checkout <commit_hash>` to checkout the commit

### Create a New Branch
1. Create a new branch with `git checkout -b <new_branch_name>`
2. This will create a new branch and checkout the commit you want to un-commit

### Revert the Changes
1. Use `git revert <commit_hash>` to revert the changes from the commit
2. This will create a new commit with the reverted changes

### Push the New Branch
1. Use `git push origin <new_branch_name>` to push the new branch
2. This will push the new branch with the reverted changes to the remote repository
