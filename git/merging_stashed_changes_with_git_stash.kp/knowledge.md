---
title: Combine the stashed changes with the current modifications using git stash
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git stash apply` to merge the stashed changes with the current changes.
---

**Contents**

[TOC]

## Stash Changes

Stashing changes allows you to temporarily store your changes away from the current branch and make them available for later use. To stash changes, use the command `git stash`.

## Merge Stashed Changes

To merge the stashed changes with the current changes, you must first apply the stashed changes to the working tree. This can be done with the command `git stash apply`. This will apply the changes to the working tree, but they will remain in the stash.

## Remove Stashed Changes

Once the stashed changes have been applied to the working tree, they can be removed from the stash with the command `git stash drop`. This will remove the changes from the stash and make them available for merging with the current changes.

## Merge Stashed Changes With Current Changes

Finally, to merge the stashed changes with the current changes, use the command `git merge <stash-name>`. This will merge the stashed changes with the current changes, allowing you to keep track of the changes you have made.
