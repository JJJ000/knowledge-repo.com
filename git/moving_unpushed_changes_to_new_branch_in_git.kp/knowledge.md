---
title: Transferring local changes that have been committed, but not yet pushed, to a new branch after pulling
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Create a new branch from the current branch, then reset the current branch to the most recent commit and push the new branch.
---

**Contents**

[TOC]

### Create a New Branch

1. Create a new branch using `git checkout -b <branch_name>`, where `<branch_name>` is the name of the new branch.

2. Checkout the new branch using `git checkout <branch_name>`.

### Stash Changes

1. Stash the committed changes using `git stash`

### Pull Changes

1. Pull the changes from the remote repository using `git pull`.

### Apply Stashed Changes

1. Apply the stashed changes to the new branch using `git stash apply`.

2. Commit the changes to the new branch using `git commit -m "<commit_message>"`, where `<commit_message>` is the commit message.
