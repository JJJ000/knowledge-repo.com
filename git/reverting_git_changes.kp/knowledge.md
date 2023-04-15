---
title: Revert all unsaved or uncommitted changes in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: No, git cannot undo all uncommitted or unsaved changes.
---

**Contents**

[TOC]

### Resetting to the Last Commit

This is the simplest way to undo all uncommitted and unsaved changes. To do this, you can use the `git reset` command. This command will reset your working directory to the last commit you made.

### Discarding Unstaged Changes

If you want to discard all of your unstaged changes, you can use the `git checkout` command. This will discard all of your changes and put your working directory back to the last commit.

### Discarding Staged Changes

If you want to discard all of your staged changes, you can use the `git reset --hard` command. This will discard all of your staged changes and put your working directory back to the last commit.

### Discarding All Changes

If you want to discard all of your changes, including both staged and unstaged changes, you can use the `git clean` command. This will discard all of your changes and put your working directory back to the last commit.
