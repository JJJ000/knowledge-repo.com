---
title: Duplicate a single branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To clone only one branch in Git, use the `-b` option followed by the branch name when running `git clone`.
---

**Contents**

[TOC]

### Cloning a Single Branch

### Step 1: Checkout the Branch
First, you need to checkout the branch that you want to clone. You can do this by running the following command: 
`git checkout <branch-name>`

### Step 2: Create a New Branch
Next, you need to create a new branch from the branch you just checked out. You can do this by running the following command: 
`git checkout -b <new-branch-name>`

### Step 3: Push the Branch to the Remote
Finally, you need to push the new branch to the remote. You can do this by running the following command: 
`git push origin <new-branch-name>`
