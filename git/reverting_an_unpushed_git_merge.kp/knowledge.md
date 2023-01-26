---
title: How to revert a git merge that has not been pushed to a remote repository yet?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: You can undo a Git merge that hasn`t been pushed yet by using the command `git merge --abort`.
---

**Contents**

[TOC]

### Reset the Merge

1. Checkout the branch you merged into.
2. Run the command `git reset --merge ORIG_HEAD`

### Revert the Merge Commit

1. Run the command `git revert -m 1 <merge_commit_sha>`

### Push the Reverted Merge

1. Push the reverted merge commit to the remote repository with `git push origin <branch_name>`

### Clean Up

1. Delete the local branch with `git branch -D <branch_name>`
2. Delete the remote branch with `git push origin --delete <branch_name>`
