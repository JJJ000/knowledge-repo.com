---
title: Rename a branch in a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To change a branch name in a Git repo, use the command `git branch -m <oldname> <newname>`.
---

**Contents**

[TOC]

### Step 1: Rename the Local Branch
1. Make sure you are on the branch you want to rename: `git checkout <old-name>`
2. Rename the branch: `git branch -m <new-name>`

### Step 2: Push the Changes to the Remote Repo
1. Push the branch to the remote repo with the new name: `git push origin <new-name>`

### Step 3: Delete the Old Branch
1. Delete the old branch from the remote repo: `git push origin --delete <old-name>`
