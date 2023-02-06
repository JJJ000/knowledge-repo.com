---
title: I made a mistake when I used 'git stash pop' which caused merge conflicts
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: If you have merge conflicts after running git stash pop, you can either resolve them manually or run git stash drop to discard the changes.
---

**Contents**

[TOC]

# Resolving Merge Conflicts
1. Check the files with conflicts: Run `git status` to find out which files have conflicts.
2. Open the conflicted files: Open the files with a text editor to view the conflicts.
3. Resolve the conflicts: Edit the files to resolve the conflicts.
4. Commit the resolved files: Run `git add` and `git commit` to save the changes.
