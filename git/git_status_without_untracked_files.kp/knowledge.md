---
title: What is the command to do a 'git status' without showing untracked files without using .gitignore?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git status -uno` command to view the status of tracked files without displaying untracked files.
---

**Contents**

[TOC]

### Removing Files from the Working Directory
1. Navigate to the repository directory in the command line.
2. Use the command `git clean -n` to view a list of untracked files.
3. Use the command `git clean -f` to remove the untracked files from the working directory.

### Updating the Git Index
1. Use the command `git reset` to reset the Git index.
2. Use the command `git add -u` to update the Git index with all the changes made in the working directory.

### Checking the Status
1. Use the command `git status` to check the status of the repository.
2. The output of the command will not include any untracked files.
