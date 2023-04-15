---
title: Temporarily remove files from git tracking
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use `git rm --cached` to untrack files from git temporarily.
---

**Contents**

[TOC]

### Step 1: Stash Changes

The first step to untrack files from git temporarily is to stash any changes that have been made to the file. This can be done by running the following command:

`git stash`

### Step 2: Remove File from Git

Next, the file needs to be removed from git. This can be done by running the following command:

`git rm --cached <filename>`

### Step 3: Restore File

Once the file has been removed from git, it can be restored by running the following command:

`git stash apply`

### Step 4: Commit Changes

Finally, the changes need to be committed to the repository by running the following command:

`git commit -m "Untracked file temporarily"`
