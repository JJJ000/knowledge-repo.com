---
title: What steps should I take to fix merge conflicts in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Resolve merge conflicts by manually editing the conflicting files to pick the desired content, then commit the result.
---

**Contents**

[TOC]

### Identifying Merge Conflicts

Merge conflicts occur when two branches of a Git repository have been modified and the changes conflict with each other. To identify merge conflicts, you can run the command `git status` to see which files have been modified in each branch. You can also use the command `git diff` to view the specific changes that have been made in each branch.

### Resolving Merge Conflicts

Once you have identified the files that have merge conflicts, you can begin to resolve them. The first step is to open the conflicting files and look for the sections of code that are causing the conflict. These sections will be marked with conflict markers, such as `<<<<<<<` and `>>>>>>>`. Once you have identified the conflicting sections, you can decide which changes to keep and which to discard. Once you have made your decision, you can remove the conflict markers and save the file.

### Committing Changes

Once you have resolved the conflicts, you can commit the changes to the repository. You can do this by running the command `git commit -m “<message>”`, where “<message>” is a short description of the changes you have made.

### Merging Branches

Once you have committed the changes, you can merge the branches together. To do this, you can run the command `git merge <branch>`, where “<branch>” is the name of the branch you want to merge. This will merge the two branches together and any conflicts will be resolved.
