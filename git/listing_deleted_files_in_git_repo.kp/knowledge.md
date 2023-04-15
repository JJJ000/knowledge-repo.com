---
title: What is the command to display a list of all the deleted files in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To list all deleted files in a Git repository, use the `git log --diff-filter=D --summary` command.
---

**Contents**

[TOC]

### Option 1: Using Git Log
1. Run the command `git log --diff-filter=D --summary` to list all the deleted files in the repository.
2. The output should list all the deleted files in the repository, along with the commit hash, author, and date.

### Option 2: Using Git Show
1. Run the command `git show --summary --name-only --pretty="format:"` to list all the deleted files in the repository.
2. The output should list all the deleted files in the repository, along with the commit hash and date.

### Option 3: Using Git Diff
1. Run the command `git diff --name-only --diff-filter=D` to list all the deleted files in the repository.
2. The output should list all the deleted files in the repository.
