---
title: What is the process for reverting a git repository to a specific commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To roll back a Git repository to a particular commit, use the command `git reset --hard <commit\_id>`.
---

**Contents**

[TOC]

### Step 1: Find the Commit Hash

The first step in rolling back a Git repository to a particular commit is to find the commit hash of the commit that you want to reset the repository to. This can be done by running the command `git log` to view the commit history and find the commit hash of the commit that you want to reset to.

### Step 2: Reset the Repository

Once you have the commit hash, you can reset the repository by running the command `git reset --hard <commit_hash>`, where `<commit_hash>` is the commit hash of the commit that you want to reset to.

### Step 3: Push the Reset

Finally, you need to push the reset to the remote repository. This can be done by running the command `git push -f origin master`, which will force push the reset to the remote repository.

### Step 4: Verify the Reset

Once the reset has been pushed to the remote repository, you can verify that the repository has been reset by running the command `git log` to view the commit history and ensure that the repository has been reset to the desired commit.
