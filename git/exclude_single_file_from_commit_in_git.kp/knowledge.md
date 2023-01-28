---
title: Include all files in a commit except for one particular file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git add .` command followed by the `git reset <file>` command to add all files to a commit except for the single specified file.
---

**Contents**

[TOC]

`**` Create a Staging Area**
1. Check the status of the repository: `git status`
2. Add all files to the staging area: `git add .`

`**` Create a Commit**
1. Create a commit with all the files in the staging area: `git commit -m "Commit message"`

`**` Unstage a File**
1. Unstage the file you don't want to commit: `git reset HEAD <file>`

`**` Create a New Commit**
1. Create a new commit with all the files except the one you unstaged: `git commit -m "Commit message"`
