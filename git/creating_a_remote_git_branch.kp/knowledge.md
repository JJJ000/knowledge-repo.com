---
title: What is the process for making a remote git branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To create a remote Git branch, use the command `git push -u origin <branch\_name>`.
---

**Contents**

[TOC]

### Step 1: Create a Local Branch

1. Checkout the branch you want to base your new branch off of: `git checkout <base_branch>`
2. Create a new branch: `git branch <new_branch>`

### Step 2: Push the New Branch to Remote

1. Push the new branch to the remote repository: `git push origin <new_branch>`

### Step 3: Checkout the New Branch

1. Checkout the new branch: `git checkout <new_branch>`

### Step 4: Push the Changes to the Remote Branch

1. Push the changes to the remote branch: `git push origin <new_branch>`
