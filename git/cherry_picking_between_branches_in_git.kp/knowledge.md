---
title: What is the process for selecting specific commits from one branch and transferring them to another branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To cherry pick from one branch to another in Git, use the `git cherry-pick <commit-id>` command.
---

**Contents**

[TOC]

# Step 1: Checkout the Target Branch

The first step in cherry-picking is to check out the target branch. This is the branch that you want to add the commits to.

# Step 2: Cherry-Pick the Commits

Once you have checked out the target branch, you can cherry-pick the commits from the source branch. To do this, use the `git cherry-pick` command followed by the SHA of the commit you want to cherry-pick.

# Step 3: Resolve Conflicts

If there are any conflicts when cherry-picking, you will need to resolve them. This is done by editing the conflicting files and then adding them to the staging area.

# Step 4: Push the Changes

Once you have resolved the conflicts and staged the changes, you can push the changes to the target branch. To do this, use the `git push` command followed by the name of the target branch.
