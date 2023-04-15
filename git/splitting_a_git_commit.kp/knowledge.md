---
title: What is the process for dividing the most recent commit into two parts in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git reset --soft HEAD~1` followed by `git commit -m <commit message>` and `git add <changed files>` for the first commit, then `git commit -m <commit message>` for the second commit.
---

**Contents**

[TOC]

### Step 1: Revert the Last Commit

Run the following command to revert the last commit:

`git revert HEAD`

This will create a new commit that undoes the changes of the previous commit.

### Step 2: Amend the Reverted Commit

Run the following command to amend the reverted commit:

`git commit --amend`

This will open up an editor for you to make changes to the commit message.

### Step 3: Create a New Commit

Run the following command to create a new commit with the changes you have made:

`git commit`

This will create a new commit with the changes you have made.

### Step 4: Push the Changes

Run the following command to push the changes to the remote repository:

`git push`

This will push the changes to the remote repository.
