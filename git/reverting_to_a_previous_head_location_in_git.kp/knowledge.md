---
title: How can I return to a previous commit and undo commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can move HEAD back to a previous location by using `git reset --hard <commit\_id>` and undo commits by using `git revert <commit\_id>`.
---

**Contents**

[TOC]

### Moving HEAD back to a Previous Location

To move the HEAD back to a previous location, you can use the `git checkout` command. This command allows you to switch between branches, and you can also specify a commit hash to move the HEAD back to a specific commit.

### Detached HEAD

When you use the `git checkout` command to move the HEAD to a specific commit, it is said to be in a detached HEAD state. This means that the HEAD is not connected to any branch, and any changes made in this state will not be tracked by Git.

### Undoing Commits

Git provides several different commands to undo commits. The `git revert` command allows you to undo a single commit by creating a new commit that undoes the changes of the specified commit. The `git reset` command allows you to undo multiple commits, and it can also be used to move the HEAD back to a previous commit. Finally, the `git clean` command can be used to remove untracked files from the working tree.
