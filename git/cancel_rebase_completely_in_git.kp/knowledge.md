---
title: Undo a rebase completely
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To completely cancel a rebase in Git, run the command `git rebase --abort`.
---

**Contents**

[TOC]

### Step 1: Abort Rebase

To abort a rebase in Git, use the command `git rebase --abort`. This command will reset the repository to its state before the rebase began.

### Step 2: Reset the Branch

Next, reset the branch to its original state with the command `git reset --hard <original-commit>`. This will reset the branch to the commit that was originally checked out before the rebase began.

### Step 3: Force Push

Force push the branch to the remote repository with the command `git push -f <remote> <branch>`. This will update the remote repository with the changes made in the reset.

### Step 4: Clean Up

Finally, clean up any local changes that may have been made during the rebase with the command `git clean -f`. This will ensure that all local changes are removed before continuing with development.
