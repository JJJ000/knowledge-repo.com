---
title: What is the best way to remove a large file from the commit history in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the git filter-branch command to remove a large file from the commit history in the Git repository.
---

**Contents**

[TOC]

### Removing the File from the Repository

1. Checkout the branch you want to remove the file from:
   `git checkout <branch name>`
2. Remove the file from the working directory:
   `git rm <file name>`
3. Commit the changes:
   `git commit -m "Removed <file name>"`

### Removing the File from the Commit History

1. Use the `git filter-branch` command to rewrite the commit history and remove the file:
   `git filter-branch --tree-filter 'rm -f <file name>' HEAD`
2. Push the changes to the remote repository:
   `git push origin <branch name> --force`

### Cleaning Up

1. Prune the Git repository to remove any unnecessary objects:
   `git gc --prune=now`
2. Verify the file has been removed:
   `git log --stat`

### Finalizing

1. Verify the file has been removed from the remote repository:
   `git ls-tree -r <branch name>`
2. Clean up any local references to the file:
   `git clean -f <file name>`
