---
title: Exclude a directory from being included in the git diff
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Exclude a directory from git diff by adding it to the .git/info/exclude file.
---

**Contents**

[TOC]

## Excluding a Directory from Git Diff

### Method 1: Using .gitignore
1. Create a `.gitignore` file in the directory which contains the directory you want to exclude from diff.
2. Add the directory name to the `.gitignore` file.
3. Commit and push the `.gitignore` file.

### Method 2: Using git update-index
1. Navigate to the parent directory of the directory you want to exclude from diff.
2. Use the command `git update-index --skip-worktree <directory-name>` to exclude the directory from diff.
3. Commit and push the changes.
