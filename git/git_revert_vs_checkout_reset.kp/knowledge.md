---
title: What are the distinctions between using git revert, checkout and reset?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git Revert creates a new commit that undoes the changes of a previous commit, Git Checkout changes the working directory to a previous commit, and Git Reset moves the current branch tip backward to a previous commit.
---

**Contents**

[TOC]

### Git Revert
Git Revert is used to undo changes in a certain commit by creating a new commit with the reverted changes. This command does not alter the existing commits, but instead creates a new commit to reverse the changes made in the specified commit.

### Git Checkout
Git Checkout is used to switch between branches or to restore working tree files. This command can be used to switch between branches, to restore files in the working directory, or to discard changes in the working directory.

### Git Reset
Git Reset is used to reset the current branch head to a specified state. This command can be used to reset the current branch head to a specified commit, to reset the staging area and working tree to the specified commit, or to discard all changes in the working tree since the specified commit.
