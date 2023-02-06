---
title: What is the procedure for cancelling a git commit when vi is open and ready for a commit message?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Press the `Esc` key, then type `q!` and press `Enter` to exit without committing.
---

**Contents**

[TOC]

# Step 1: Exit VI
1. Press the `esc` key to enter command mode.
2. Type `:q!` and press `enter` to exit VI without saving any changes.

# Step 2: Abort the Commit
3. Type `git commit --abort` and press `enter` to abort the commit.

# Step 3: Check Status
4. Type `git status` and press `enter` to view the status of your repository.
