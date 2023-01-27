---
title: Discard local commits in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To discard local commits, use the `git reset --hard` command.
---

**Contents**

[TOC]

### Discard Local Commits
Discarding local commits in Git is a fairly straightforward process.

### Step 1: Checkout the Branch
The first step is to checkout the branch that contains the commits you want to discard. This can be done by running the command `git checkout <branch-name>`.

### Step 2: Reset the Branch
Once the branch is checked out, you can reset it to the commit before the one you want to discard. This can be done by running the command `git reset --hard <commit-hash>`.

### Step 3: Push the Changes
Finally, you can push the changes to the remote repository by running the command `git push --force`. This will overwrite any commits that were previously pushed to the remote branch.
