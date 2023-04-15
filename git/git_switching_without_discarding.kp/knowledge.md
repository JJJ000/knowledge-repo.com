---
title: Switch to a different branch in git without losing local changes
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use `git stash` to temporarily save your local changes, then switch branches, and then use `git stash pop` to reapply them.
---

**Contents**

[TOC]

#1 Check for Unstaged Changes

Before switching branches, it is important to check for any unstaged changes in the current branch. To check for any unstaged changes, use the `git status` command to list any modified files that have not been added to the staging area.

#2 Stash Changes

If there are any unstaged changes, they must be stashed using the `git stash` command. This will store the changes in a temporary area and allow the user to switch branches without discarding the local changes.

#3 Switch Branches

Once the changes have been stashed, the user can switch branches by using the `git checkout` command and specifying the name of the branch to switch to.

#4 Unstash Changes

Once the user has switched branches, they can then unstash the changes by using the `git stash pop` command. This will restore the changes to the local working directory.
