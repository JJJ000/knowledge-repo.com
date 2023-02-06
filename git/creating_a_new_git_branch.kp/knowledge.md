---
title: Create a new git branch and add the current changes to it
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a new branch with `git checkout -b <branch-name>` and then commit your changes to the new branch.
---

**Contents**

[TOC]

# Creating a New Branch

1. Check the current branch: `git branch`
2. Create a new branch: `git checkout -b <branch_name>`
3. Add the changes to the new branch: `git add .`
4. Commit the changes: `git commit -m “<commit_message>”`

# Switching to the New Branch

1. Check the current branch: `git branch`
2. Switch to the new branch: `git checkout <branch_name>`

# Pushing the New Branch

1. Push the new branch: `git push -u origin <branch_name>`
2. Check the remote branches: `git branch -r`
