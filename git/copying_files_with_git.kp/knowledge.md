---
title: Copy all files in a directory from another branch using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Checkout the desired branch and run `git checkout <branch> <directory>/*` to copy all files in the directory from another branch.
---

**Contents**

[TOC]

## Using `git checkout`
1. Checkout the branch you want to copy files from: `git checkout <branch-name>`
2. Navigate to the directory containing the files you want to copy: `cd <directory-name>`
3. Copy all the files from the directory: `git checkout .`

## Using `git show`
1. Checkout the branch you want to copy files from: `git checkout <branch-name>`
2. Navigate to the directory containing the files you want to copy: `cd <directory-name>`
3. List the files in the directory: `git show --name-only`
4. Copy each file from the branch: `git show <branch-name>:<file-name> > <file-name>`
