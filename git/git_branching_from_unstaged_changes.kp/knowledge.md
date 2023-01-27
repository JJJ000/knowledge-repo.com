---
title: Create a new branch from the current, unsaved changes on the master branch in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can create a new branch from unstaged/uncommitted changes on master by using the `git checkout -b <branch\_name>` command.
---

**Contents**

[TOC]

### Step 1: Stash changes

The first step is to stash any changes that have been made to the master branch. This can be done by running the command `git stash` in the terminal.

### Step 2: Create Branch

Next, create a new branch from the master branch. This can be done by running the command `git checkout -b <branch-name>` in the terminal.

### Step 3: Apply Stashed Changes

Finally, apply the stashed changes to the newly created branch. This can be done by running the command `git stash pop` in the terminal.
