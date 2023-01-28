---
title: Undo a particular commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To remove a specific commit, use the `git revert` command.
---

**Contents**

[TOC]

### Using Revert
1. Find the commit you want to remove.
2. Run git revert <commit-hash>.
3. Push the changes with git push.

### Using Reset
1. Find the commit you want to remove.
2. Run git reset <commit-hash>.
3. Push the changes with git push --force.
