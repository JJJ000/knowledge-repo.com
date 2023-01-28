---
title: What is the best way to prevent my local changes from being overwritten when I run 'git pull' and I get an error about them being overwritten by a merge?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use the `--no-commit` flag to pull without automatically committing any changes.
---

**Contents**

[TOC]

### Solution

### Step 1: Stash Local Changes

The first step to avoiding overwriting local changes when performing a `git pull` is to stash any local changes that have been made. This can be done by running the command `git stash` from the command line.

### Step 2: Pull from Remote

Once the local changes have been stashed, the next step is to pull from the remote repository. This can be done by running the command `git pull` from the command line.

### Step 3: Reapply Local Changes

After the pull from the remote is complete, the local changes can be reapplied by running the command `git stash pop` from the command line. This will restore the local changes that were stashed in the first step.

### Step 4: Resolve Conflicts

In some cases, there may be conflicts between the local changes and the changes pulled from the remote. If this is the case, the conflicts will need to be manually resolved before the changes can be committed.
