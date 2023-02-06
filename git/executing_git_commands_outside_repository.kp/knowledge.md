---
title: What is the procedure for running a git command without being in the repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can execute a Git command by specifying the path to the repository with the `--git-dir` flag.
---

**Contents**

[TOC]

## Option 1: Using the Full Path
1. Determine the full path of the repository you wish to execute the command in.
2. Enter the command `git -C <full path> <command>`

## Option 2: Setting the GIT_DIR Environment Variable
1. Determine the full path of the repository you wish to execute the command in.
2. Set the environment variable `GIT_DIR` to the full path of the repository.
3. Enter the command `git <command>`
