---
title: How to revert a specific file to its previous version before changes were made locally
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To undo local changes to a specific file in Git, use the `git checkout -- <file>` command.
---

**Contents**

[TOC]

### Step 1: Check the Status

Before undoing any changes, it is important to check the status of the file in Git to make sure the changes have been committed. This can be done with the command `git status`.

### Step 2: Checkout the File

If the changes have been committed, the next step is to checkout the file. This can be done with the command `git checkout <file-name>`.

### Step 3: Reset the File

The next step is to reset the file to its previous committed state. This can be done with the command `git reset <file-name>`.

### Step 4: Commit the Changes

Finally, the changes need to be committed to the repository. This can be done with the command `git commit -m "<commit message>"`.
