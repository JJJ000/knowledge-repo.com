---
title: What steps should I take to address git's message that I need to "commit my changes or stash them before I can merge"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You must commit or stash your changes before you can merge.
---

**Contents**

[TOC]

### Stashing Changes

Stashing changes is a way of temporarily saving changes that you have made in your working directory so that you can switch branches or pull in upstream changes without losing your work. To do this, use the `git stash` command.

### Committing Changes

Committing changes is a way of permanently saving the changes that you have made in your working directory. To do this, use the `git commit` command.

### Merging Branches

Once you have either stashed or committed your changes, you can merge the branches together. To do this, use the `git merge` command.

### Resolving Conflicts

If there are any conflicts between the two branches, you will need to resolve them before you can complete the merge. To do this, use the `git mergetool` command.
