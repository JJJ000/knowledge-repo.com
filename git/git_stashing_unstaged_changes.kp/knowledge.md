---
title: How can I save all my unsaved changes using git stash?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To put away all unstaged changes, use the command `git stash --include-untracked`.
---

**Contents**

[TOC]

# Step 1: Stash Unstaged Changes
To stash unstaged changes, use the command `git stash`. This command will save all of your changes that have not been staged in a special area called the stash.

# Step 2: Check the Status
To check the status of your stash, use the command `git status`. This command will show you the current state of your repository and the changes that are in your stash.

# Step 3: Unstash Changes
To unstash changes, use the command `git stash pop`. This command will take the changes from your stash and apply them to your working tree.

# Step 4: Commit Changes
Finally, to commit the changes that you have unstashed, use the command `git commit`. This command will add the changes to your repository and make them part of your project's history.
