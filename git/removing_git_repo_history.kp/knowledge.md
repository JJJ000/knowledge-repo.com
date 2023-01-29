---
title: What is the best way to clear the past commits from a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To remove the old history from a git repository, use the `git reset --hard` command.
---

**Contents**

[TOC]

### Delete the Git History Locally
1. Make sure you have a backup of your repository.
2. Check out a new branch from the master branch: `git checkout -b new_branch`.
3. Delete the `.git` directory: `rm -rf .git`.
4. Re-initialize Git in the repository: `git init`.

### Push the New History to the Remote Repository
1. Add the remote repository: `git remote add origin <remote-repository-url>`.
2. Push the new branch to the remote repository: `git push -u origin new_branch`.

### Rebase the Master Branch
1. Check out the master branch: `git checkout master`.
2. Rebase the master branch onto the new branch: `git rebase new_branch`.
3. Push the rebased master branch to the remote repository: `git push -f origin master`.

### Clean Up
1. Delete the new branch: `git branch -D new_branch`.
2. Fetch the latest changes from the remote repository: `git fetch origin`.
