---
title: What is the best way to format a patch using my stored items?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can apply the changes stashed away in Git with the `git stash apply` command.
---

**Contents**

[TOC]

# Section 1: Stashing Changes

To stash away changes in Git, you can use the `git stash` command. This will store away any uncommitted changes you have made in your working directory, allowing you to switch branches or do other tasks without losing your changes.

# Section 2: Viewing Stashed Changes

If you want to view the changes that you have stashed away, you can use the `git stash list` command. This will show you a list of all the stashed changes, along with a unique identifier for each change.

# Section 3: Applying Stashed Changes

To apply stashed changes to your working directory, you can use the `git stash apply` command. This will take the changes from the stash and apply them to your working directory, allowing you to continue working on them.

# Section 4: Removing Stashed Changes

If you no longer need the stashed changes, you can use the `git stash drop` command. This will remove the stashed changes from the stash, freeing up space and allowing you to focus on other tasks.
