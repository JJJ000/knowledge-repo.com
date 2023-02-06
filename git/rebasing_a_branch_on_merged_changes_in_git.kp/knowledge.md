---
title: What is the process for incorporating the changes of the current branch on top of the changes being merged in?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git rebase <branch\_name>` to rebase the current branch`s changes on top of the changes being merged in.
---

**Contents**

[TOC]

# Step 1: Fetch Latest Changes 

Run `git fetch` to get the latest changes from the remote repository.

# Step 2: Rebase Current Branch 

Run `git rebase <branch_name>` to rebase the current branch's changes on top of the changes being merged in. 

# Step 3: Resolve Conflicts 

If there are conflicts, resolve them by editing the conflicting files and running `git add <file_name>` to add the resolved files.

# Step 4: Continue Rebase 

Run `git rebase --continue` to continue the rebase process.
