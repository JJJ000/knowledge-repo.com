---
title: What is the command to undo the last git add?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can undo the last git add by running the command `git reset HEAD <file>`.
---

**Contents**

[TOC]

**Option 1:**

##### Using `git reset`
1. Run `git reset` in the terminal.
2. This will remove all changes that have been staged using `git add`.

**Option 2:**

##### Using `git reset HEAD`
1. Run `git reset HEAD` in the terminal.
2. This will remove the last change that was added to the staging area.
