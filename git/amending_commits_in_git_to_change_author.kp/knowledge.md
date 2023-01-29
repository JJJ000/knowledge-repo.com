---
title: How to alter the author of multiple commits in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `git rebase -i` command to amend multiple commits and change the author.
---

**Contents**

[TOC]

### Step 1: Revert the commits

Use the `git revert` command to revert the commits you want to change. This will create a new commit that undoes the changes in the original commit, and then you can modify the commit message and author.

### Step 2: Amend the commit

Use the `git commit --amend` command to amend the commit. This will open up a text editor to let you modify the commit message and author.

### Step 3: Push the changes

Once you are satisfied with the changes, use the `git push` command to push the changes to the remote repository.

### Step 4: Clean up

If you have reverted any commits, you can use the `git reset` command to clean up your local repository.
