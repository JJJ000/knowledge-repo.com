---
title: Replace existing files when using 'git stash'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, it is not possible to force git stash to overwrite added files.
---

**Contents**

[TOC]

**Option 1:**
1. Use `git stash` to save the changes.
2. Use `git reset --hard` to discard the added files.
3. Execute `git stash pop` to restore the changes.

**Option 2:**
1. Use `git stash --include-untracked` to save the changes.
2. Use `git reset --hard` to discard the added files.
3. Execute `git stash pop` to restore the changes.
