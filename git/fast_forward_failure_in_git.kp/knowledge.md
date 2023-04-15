---
title: It is not possible to proceed quickly, so the process must be aborted
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git will not allow a fast-forward merge and will abort the process.
---

**Contents**

[TOC]

### What is Fast-Forwarding
Fast-forwarding is a feature in Git which allows the branch pointer to be moved to the most recent commit on a different branch without creating a merge commit. This is achieved by simply moving the branch pointer to the tip of the other branch.

### When is Fast-Forwarding Not Possible
Fast-forwarding is not possible when the branch pointer is behind the tip of the other branch. This can happen when there are commits on the other branch which have not been merged into the current branch.

### Why is Fast-Forwarding Aborted
Fast-forwarding is aborted because it would cause the branch pointer to skip over commits which have not been merged into the current branch. This could lead to data loss or other unexpected behavior.

### How to Resolve
In order to resolve the issue, the commits on the other branch must be merged into the current branch. This can be done by using a merge commit or by rebasing the current branch onto the other branch.
