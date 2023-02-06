---
title: What is the process for using the 'onto' command to rebase a branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To git rebase a branch with the onto command, run `git rebase <branch> <onto>`.
---

**Contents**

[TOC]

# Step 1: Checkout the Branch to Rebase

To start the rebase process, you must first checkout the branch you want to rebase. This can be done using the `git checkout` command.

# Step 2: Rebase the Branch

Once the branch is checked out, you can use the `git rebase` command with the `--onto` flag to rebase the branch onto another branch. The `--onto` flag requires two arguments, the first being the branch or commit you want to rebase onto, and the second being the branch or commit you want to rebase from.

# Step 3: Resolve Conflicts

During the rebasing process, conflicts may arise. If this is the case, you must resolve the conflicts before the rebase can complete. To do this, you can use the `git mergetool` command to launch a graphical tool that will help you resolve the conflicts.

# Step 4: Complete the Rebase

Once the conflicts have been resolved, you can complete the rebase by running the `git rebase --continue` command. This will finish the rebase process and your branch will be rebased onto the other branch.
