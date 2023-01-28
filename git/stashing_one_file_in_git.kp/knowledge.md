---
title: Store a single file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can stash a single file in Git using the command `git stash push <file>`.
---

**Contents**

[TOC]

### Stashing a Single File

### Step 1: Add File to Stash

To add a single file to the stash, run the following command in a terminal window:

`git stash push <file_name>`

This will add the specified file to the stash.

### Step 2: Apply Stashed File

To apply the stashed file, run the following command in a terminal window:

`git stash apply`

This will apply the stashed file to the working tree.

### Step 3: Remove Stashed File

To remove the stashed file, run the following command in a terminal window:

`git stash drop`

This will remove the stashed file from the stash.
