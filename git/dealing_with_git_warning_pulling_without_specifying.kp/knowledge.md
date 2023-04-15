---
title: What is the best way to address the git warning that suggests avoiding pulling without specifying how to merge conflicting branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Specify a merge strategy when pulling to reconcile divergent branches.
---

**Contents**

[TOC]

### Solution 1: Use Merge

When pulling without specifying how to reconcile divergent branches, the best way to deal with this warning is to use the `git merge` command. This command will combine the changes from both branches into a single branch, allowing you to keep the changes from both branches without losing any of them.

### Solution 2: Rebase

Another way to deal with this warning is to use the `git rebase` command. This command will take the changes from one branch and apply them to the other branch, allowing you to keep the changes from both branches without losing any of them.

### Solution 3: Reset

The last option for dealing with this warning is to use the `git reset` command. This command will reset the branch to the last commit, discarding any changes that were made since then. This should only be used as a last resort, as it can cause data loss if the changes were important.

### Solution 4: Avoid Pulling Without Specifying

The best way to deal with this warning is to simply avoid pulling without specifying how to reconcile divergent branches. Always specify the desired merge strategy when pulling, and if you are unsure of which strategy to use, consult the documentation for the version of Git that you are using.
