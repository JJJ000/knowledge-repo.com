---
title: How can I undo unstaged changes in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To discard unstaged changes in Git, use the command `git checkout -- <file>`.
---

**Contents**

[TOC]

### Discard Unstaged Changes

### Step 1: Check Status

The first step is to check the status of your repository. This can be done by running the command `git status`. This will display any unstaged changes that have been made.

### Step 2: Discard Unstaged Changes

Once you have identified the changes that you would like to discard, you can use the command `git checkout -- <file>` to discard the changes. This command will discard any unstaged changes made to the specified file. 

### Step 3: Confirm Changes

To confirm that the changes have been discarded, you can again run the command `git status`. This will display the current status of your repository and any changes that have not been committed.

### Step 4: Commit Changes

Finally, you can commit the changes to your repository by running the command `git commit -m "<message>"`. This will commit any changes that have been made and the message that you provide will be the commit message.
