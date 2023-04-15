---
title: Revert to a previous git commit in a public repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To rollback to an old Git commit in a public repo, you can use the `git revert` command.
---

**Contents**

[TOC]

### Step 1: Checkout the Old Commit

The first step to rollback to an old Git commit in a public repo is to checkout the commit you want to rollback to. To do this, you can use the `git checkout` command followed by the commit hash.

### Step 2: Create a New Branch

Once you have checked out the old commit, the next step is to create a new branch from the old commit. This can be done using the `git branch` command followed by the new branch name.

### Step 3: Push the New Branch

Once the new branch has been created, the next step is to push the new branch to the public repo. This can be done using the `git push` command followed by the new branch name.

### Step 4: Merge the New Branch

The final step is to merge the new branch into the main branch of the public repo. This can be done using the `git merge` command followed by the new branch name.
