---
title: What is the process for undoing a stash pop?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git stash drop` to abort the stash pop.
---

**Contents**

[TOC]

### Aborting a Stash Pop

### Step 1: Retrieve the Stashed Changes 
The first step is to retrieve the stashed changes that were previously stashed away. This can be done by running the command `git stash list` to view the list of stashed changes.

### Step 2: Re-Stash the Changes
Once the stashed changes have been retrieved, the next step is to re-stash them away. This can be done by running the command `git stash push` with the same parameters that were used when the changes were originally stashed away.

### Step 3: Discard the Stash
Once the changes have been re-stashed, the next step is to discard the stash. This can be done by running the command `git stash drop` with the same parameters that were used when the changes were originally stashed away.

### Step 4: Restore the Working Directory
Finally, the working directory can be restored to its previous state by running the command `git reset --hard` to discard any changes that may have been made while attempting to pop the stash.
