---
title: What is the process for locating a branch point using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: A branch point can be found in Git by using the command `git branch -a` to list all branches.
---

**Contents**

[TOC]

### Using the 'git log' Command
The `git log` command can be used to find a branch point in a repository. This command displays the history of commits in the repository. It can be used to find the most recent commit that is shared between two branches. 

### Using the 'git merge-base' Command
The `git merge-base` command can also be used to find a branch point between two branches. This command will return the most recent commit that is shared between the two branches. 

### Using the 'git show-branch' Command
The `git show-branch` command can be used to display the history of commits in a repository. This command will show the commits that are shared between two branches. It can be used to find the most recent commit that is shared between the two branches.

### Using the 'git branch --contains' Command
The `git branch --contains` command can be used to find the branch point between two branches. This command will return the most recent commit that is shared between the two branches.
