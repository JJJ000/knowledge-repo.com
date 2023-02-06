---
title: What is the process for deleting a branch on my local machine?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the command `git branch -d <branch\_name>` to remove a branch locally in Git.
---

**Contents**

[TOC]

# Step 1: Delete the Local Branch

1. Open the terminal.
2. Type `git branch -d [branch_name]` to delete the local branch.

# Step 2: Delete the Remote Branch

1. Open the terminal.
2. Type `git push origin --delete [branch_name]` to delete the remote branch.
