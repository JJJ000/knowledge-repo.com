---
title: What is the process for deleting an incorrect remote branch reference in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run the command `git remote prune <remote>` to remove any invalid remote branch references from Git.
---

**Contents**

[TOC]

### Using Git
1. Check the local branches with `git branch -a`.
2. Find the invalid remote branch reference and delete it with `git branch -d <branch_name>`.
3. Push the updated local branches to the remote repository with `git push origin --all`.

### Using Git CLI
1. Check the local branches with `git branch -a`.
2. Remove the invalid remote branch reference with `git remote rm <branch_name>`.
3. Push the updated local branches to the remote repository with `git push origin --all`.
