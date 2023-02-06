---
title: It is not possible to proceed with a git rebase merge conflict
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git rebase conflicts must be resolved before the rebase can continue.
---

**Contents**

[TOC]

## Resolving the Conflict
1. Check the conflicting files to determine which changes should be kept and which should be discarded.
2. Use a text editor or a version control tool to manually resolve the conflicts.
3. Once the conflicts have been resolved, add the resolved files to the staging area.
4. Continue the rebase process by running `git rebase --continue`.

## What if the Conflict Cannot be Resolved?
1. Abort the rebase process by running `git rebase --abort`.
2. Restore the original branch by running `git reset --hard ORIG_HEAD`.
3. Rebase the branch from the beginning by running `git rebase --onto NEW_BASE ORIG_HEAD`.
4. If the conflict still cannot be resolved, you may need to abandon the rebase and merge the branches using a regular merge.
