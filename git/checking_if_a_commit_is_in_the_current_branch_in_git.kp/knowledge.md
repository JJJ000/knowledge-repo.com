---
title: How can I tell if the current branch contains a specific commit using its id?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git branch --contains <commit\_id>` to determine if the current branch contains the given commit.
---

**Contents**

[TOC]

### Using git log

1. Run `git log` in the terminal.
2. Look for the commit ID in the output of the command.
3. If the commit ID is present, then the current branch contains the commit.

### Using git branch

1. Run `git branch -a` in the terminal.
2. Look for the commit ID in the output of the command.
3. If the commit ID is present, then the current branch contains the commit.
