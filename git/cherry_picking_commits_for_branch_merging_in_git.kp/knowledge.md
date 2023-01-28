---
title: What is the process for selecting specific commits and merging them into a different branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To cherry-pick a range of commits and merge them into another branch in Git, use the command `git cherry-pick <commit range> && git checkout <branch> && git merge <branch>`.
---

**Contents**

[TOC]

### Step 1: Checkout the Source Branch

First, you need to checkout the source branch from which you want to cherry-pick the commits. To do this, you can use the `git checkout` command followed by the name of the source branch.

### Step 2: Select Commits

Next, you need to select the commits you want to cherry-pick. You can use the `git log` command to view the list of commits in the source branch. Then, you can use the `git cherry-pick` command followed by the commit hashes of the commits you want to cherry-pick.

### Step 3: Checkout the Target Branch

After selecting the commits, you need to checkout the target branch in which you want to merge the cherry-picked commits. To do this, you can use the `git checkout` command followed by the name of the target branch.

### Step 4: Merge Commits

Finally, you need to merge the cherry-picked commits into the target branch. To do this, you can use the `git merge` command followed by the name of the source branch. This will merge the commits into the target branch.
