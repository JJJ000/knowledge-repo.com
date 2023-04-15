---
title: How to transfer uncommitted work to a new branch in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Create a new branch, then use `git cherry-pick` to move the existing work to the new branch.
---

**Contents**

[TOC]

### Create a New Branch
1. Checkout the current branch: `git checkout <branch_name>`
2. Create a new branch: `git branch <new_branch_name>`
3. Checkout the new branch: `git checkout <new_branch_name>`

### Move Uncommitted Work
1. Stage all changes: `git add .`
2. Commit the changes to the new branch: `git commit -m "message"`

### Push the New Branch
1. Push the new branch to the remote repository: `git push -u origin <new_branch_name>`

### Switch Back to the Original Branch
1. Checkout the original branch: `git checkout <original_branch_name>`
