---
title: Revert all modifications made since the last commit in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To reset all changes after the last commit, use the `git reset --hard HEAD` command.
---

**Contents**

[TOC]

### Resetting to a Previous Commit

1. Check the commit history to find the commit you want to reset to: `git log`
2. Use `git reset` to reset to the desired commit: `git reset <commit_hash>`

### Unstaging Changes

1. Unstage all changes since the last commit: `git reset HEAD`
2. Unstage a single file: `git reset HEAD <file>`

### Discarding Local Changes

1. Discard all local changes in your working directory: `git checkout -- .`
2. Discard local changes in a single file: `git checkout -- <file>`
