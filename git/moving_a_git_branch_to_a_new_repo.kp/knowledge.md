---
title: What is the process for taking a git branch and creating a separate repository for it?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To move a Git branch out into its own repository, use the `git clone --single-branch` command.
---

**Contents**

[TOC]

# 1. Clone the Repository
Clone the repository that contains the branch you want to move out into its own repository.

# 2. Checkout the Branch
Checkout the branch you want to move out into its own repository and make sure it is the active branch.

# 3. Create a New Repository
Create a new repository in which to move the branch.

# 4. Push the Branch
Push the branch to the new repository using the command `git push <new_repo> <branch_name>`. This will push the branch and its history to the new repository.
