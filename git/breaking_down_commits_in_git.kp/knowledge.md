---
title: Divide a previous commit into multiple commits
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git rebase -i <commit\_id>`, then change the `pick` command to `edit` or `reword` for the commit you wish to split.
---

**Contents**

[TOC]

### Step 1: Find the Commit

To break a previous commit into multiple commits in Git, the first step is to find the commit that you wish to break. You can do this by running the command `git log` to view the history of your commits. 

### Step 2: Revert the Commit

Once you have identified the commit that you want to break, you can use the command `git revert <commit-hash>` to revert the commit. This will create a new commit that reverts the changes from the original commit.

### Step 3: Amend the Commit

Next, you can use the command `git commit --amend` to amend the reverted commit. This will open your text editor of choice, allowing you to make changes to the commit message. 

### Step 4: Push the Changes

Once you have finished making changes to the commit message, you can use the command `git push` to push the changes to your remote repository. This will update the history of your commits with the new changes.
