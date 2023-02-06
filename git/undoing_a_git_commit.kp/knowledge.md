---
title: What is the command to revert the last commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To undo the last commit in git, use the command `git reset --hard HEAD~1`.
---

**Contents**

[TOC]

# Undoing the Last Commit

## Option 1: Soft Reset
A soft reset can be done by using the `git reset --soft HEAD~1` command. This will move the HEAD pointer back one commit and reset the index to the same commit. This will leave the working directory untouched, so any changes made since the last commit will still be present.

## Option 2: Hard Reset
A hard reset can be done by using the `git reset --hard HEAD~1` command. This will move the HEAD pointer back one commit and reset the index and working directory to the same commit. This will discard any changes made since the last commit.

## Option 3: Revert
A revert can be done by using the `git revert HEAD` command. This will create a new commit that undoes the changes made in the last commit. This is useful if you want to keep a record of the changes that were made and undone.

## Option 4: Checkout
A checkout can be done by using the `git checkout HEAD~1` command. This will move the HEAD pointer back one commit and reset the index and working directory to the same commit. This will discard any changes made since the last commit.
