---
title: What is the process for canceling a cherry-pick?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To abort a cherry-pick in Git, use the command `git cherry-pick --abort`.
---

**Contents**

[TOC]

### Aborting a Cherry-Pick

### Step 1: Check the Status

Before attempting to abort a cherry-pick, it is important to check the status of the repository. This can be done by running the `git status` command. This will show any changes that have been made to the repository since the cherry-pick was started.

### Step 2: Reset the Repository

If the repository has not been changed since the cherry-pick began, then it can be reset to its original state. This can be done by running the `git reset --hard` command. This will discard any changes that have been made since the cherry-pick began.

### Step 3: Revert the Commit

If the repository has been changed since the cherry-pick began, then it is necessary to revert the commit. This can be done by running the `git revert <commit-hash>` command, where `<commit-hash>` is the hash of the commit that was cherry-picked. This will revert the changes made by the cherry-picked commit.

### Step 4: Clean Up

Once the repository has been reset or the commit has been reverted, it is necessary to clean up any files that were created during the cherry-pick. This can be done by running the `git clean -f` command. This will delete any untracked files that were created during the cherry-pick.
