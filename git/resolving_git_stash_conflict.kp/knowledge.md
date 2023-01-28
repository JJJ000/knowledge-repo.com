---
title: What is the best way to fix a git stash conflict without committing?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can resolve a git stash conflict by running `git stash show -p` and manually merging the changes.
---

**Contents**

[TOC]

### Section 1 - Stash Changes

The first step to resolving a git stash conflict is to stash any changes that you have made in the current branch. This can be done by typing the following command in the terminal:

`git stash`

This command will save any uncommitted changes in the current branch and remove them from the working tree.

### Section 2 - Rebase

The next step is to rebase the changes from the stash onto the current branch. This can be done by typing the following command in the terminal:

`git rebase --onto <branch> <stash>`

Replace `<branch>` with the name of the branch that you wish to rebase the changes onto and `<stash>` with the name of the stash that you wish to rebase.

### Section 3 - Resolve Conflicts

Once the rebase is complete, you will need to resolve any conflicts that may have been caused by the rebase. This can be done by using a text editor to manually edit the files that have conflicts.

### Section 4 - Apply Stash

Once the conflicts have been resolved, the final step is to apply the stash. This can be done by typing the following command in the terminal:

`git stash apply`

This command will apply the changes from the stash onto the current branch.
