---
title: Reverting a previously merged git commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To re-do a reverted merge in Git, use the `git revert` command to revert the merge, then use `git merge` to re-perform the merge.
---

**Contents**

[TOC]

### Step 1: Revert Merge

First, you need to revert the merge that you want to redo. To do this, you can use the `git revert` command. This will create a new commit that undoes the changes made by the merge commit.

### Step 2: Checkout the Reverted Merge

Once you have reverted the merge, you need to check out the reverted merge commit. This can be done using the `git checkout` command. This will checkout the reverted merge commit, allowing you to make changes to it.

### Step 3: Redo the Merge

Once you have checked out the reverted merge commit, you can redo the merge. To do this, you can use the `git merge` command. This will allow you to merge the two branches that were previously merged.

### Step 4: Push the Changes

Once you have redone the merge, you need to push the changes to the remote repository. This can be done using the `git push` command. This will push the changes to the remote repository, allowing other people to see the changes you have made.
