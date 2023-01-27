---
title: What is the process for storing an untracked file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To stash an untracked file in Git, use the command `git stash push <file>`.
---

**Contents**

[TOC]

### Stashing Untracked Files

### Step 1: Add the Untracked File

The first step in stashing an untracked file is to add it to the staging area. This can be done by running the command `git add <filename>`.

### Step 2: Stash the File

Once the file has been added, it can be stashed with the command `git stash`. This command will save all of the changes that have been made to the repository, including the untracked file.

### Step 3: Apply the Stash

The stashed changes can then be applied to the repository by running the command `git stash apply`. This will restore the repository to the state it was in prior to the changes being stashed.

### Step 4: Remove the Stash

Finally, the stashed changes can be removed from the repository by running the command `git stash drop`. This will remove the stashed changes from the repository and allow the repository to return to its original state.
