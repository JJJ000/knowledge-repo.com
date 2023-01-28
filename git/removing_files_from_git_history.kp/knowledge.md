---
title: What is the process for deleting a file from git's records?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git filter-branch` command to remove a file from the Git history.
---

**Contents**

[TOC]

### Remove the File from the Repository

1. Navigate to the root directory of the repository.
2. Use the command `git rm <file>` to remove the file from the repository.
3. Commit the changes with the command `git commit -m "Removed <file> from repository"`.

### Remove the File from the Git History

1. Use the command `git filter-branch --index-filter 'git rm --cached --ignore-unmatch <file>' --prune-empty --tag-name-filter cat -- --all` to remove the file from the Git history.
2. Force push the changes with the command `git push origin --force --all`.

### Clean Up the Repository

1. Use the command `git for-each-ref --format="%(refname)" refs/original/ | xargs -n 1 git update-ref -d` to clean up the repository.
2. Force push the changes with the command `git push origin --force --all`.

### Verify the Changes

1. Use the command `git log --diff-filter=D --summary` to verify that the file has been removed from the Git history.
