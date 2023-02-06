---
title: What is the process for creating a git repository with a branch name other than "master"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can create a Git repository with a custom default branch name using the command `git init --initial-branch <name>`.
---

**Contents**

[TOC]

### Step 1: Create a Local Repository

1. Create a folder for your repository and navigate to it in the terminal.
2. Initialize the local repository with the `git init` command.

### Step 2: Configure the Default Branch

1. Run the `git symbolic-ref HEAD` command to display the current default branch name.
2. Use the `git symbolic-ref HEAD refs/heads/<branch_name>` command to set the default branch name to the desired branch name.

### Step 3: Push the Repository to Remote

1. Create a remote repository on your Git hosting provider.
2. Add the remote repository to your local repository with the `git remote add origin <repo_url>` command.
3. Push the local repository to the remote repository with the `git push -u origin master` command.

### Step 4: Verify the Default Branch

1. Run the `git symbolic-ref HEAD` command to verify that the default branch name has been changed.
