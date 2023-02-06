---
title: Upload an existing project to github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a new repository on Github, then use the command line to push an existing local project to the remote repository.
---

**Contents**

[TOC]

# Step 1: Create a New Repository on GitHub
1. Log into GitHub and create a new repository.
2. Give the repository a name and description.

# Step 2: Initialize the Local Repository
1. Open the terminal and navigate to the directory of the project you want to push.
2. Initialize the directory as a Git repository by running `git init`.

# Step 3: Add the Remote
1. Add the remote repository with `git remote add origin <remote repository URL>`.
2. Verify the remote was added correctly by running `git remote -v`.

# Step 4: Push the Changes
1. Add files to the repository with `git add .`.
2. Commit the changes with `git commit -m "Commit message"`.
3. Push the changes to the remote repository with `git push origin master`.
