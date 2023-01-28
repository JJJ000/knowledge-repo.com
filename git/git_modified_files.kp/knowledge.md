---
title: Retrieve all files that have been altered in the git branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git log --name-only --oneline -- <branch\_name>` to get a list of all files that have been modified in the specified git branch.
---

**Contents**

[TOC]

### Using Git Log

You can use the `git log` command to list all the files that have been modified in a git branch. This command will list all the commits in the branch, including the files that have been modified in each commit.

### Using Git Show

You can also use the `git show` command to list all the files that have been modified in a git branch. This command will list the files that have been modified in the most recent commit.

### Using Git Diff

You can also use the `git diff` command to list all the files that have been modified in a git branch. This command will list all the changes that have been made to the files since the last commit.

### Using Git Status

You can also use the `git status` command to list all the files that have been modified in a git branch. This command will list all the files that have been modified and are staged for the next commit.
