---
title: What is the difference between a git fast-forward merge and a no fast-forward merge?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: A fast-forward merge keeps the branch history linear, while a non-fast-forward merge creates a merge commit to signify the point at which the branches were joined.
---

**Contents**

[TOC]

### Fast-Forward Merge
A fast-forward merge is a type of merge that moves the current branch pointer to the target branch. This is the default behavior of Git when there are no conflicts. This type of merge does not create a merge commit and will not preserve the history of the two branches.

### No Fast-Forward Merge
A no fast-forward merge is a type of merge that creates a new commit with two parent commits. This type of merge will preserve the history of both branches and will create a merge commit. This is the default behavior of Git when there are conflicts.
