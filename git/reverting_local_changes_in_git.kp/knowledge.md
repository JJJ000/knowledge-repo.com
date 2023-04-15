---
title: What is the best way to reset my local git managed project to its previous state?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git reset --hard HEAD` to revert all local changes to the last commit.
---

**Contents**

[TOC]

### Step 1: Stash Local Changes

If you have any changes that you would like to keep, you should first `git stash` them. This will save your local changes to a "stash" which you can access later.

### Step 2: Reset to Previous Commit

To revert all local changes to the previous commit, you can use the `git reset --hard` command. This will reset your local repository to the previous commit and discard any local changes.

### Step 3: Reapply Stashed Changes

If you have stashed any changes in Step 1, you can reapply them using the `git stash pop` command. This will reapply the stashed changes to your local repository.

### Step 4: Push Changes

Finally, you can push the changes to the remote repository using the `git push` command. This will update the remote repository with the changes you have made.
