---
title: What is the child commit of the given reference in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To find the next commit (child/children of ref) in Git, use the `git log` command with the `--children` option.
---

**Contents**

[TOC]

### Using git log

1. Run `git log` in the command line.
2. Look for the commit that you want to find the children of.
3. Copy the SHA of the commit.
4. Run `git log --oneline --decorate --children <commit-SHA>`.

### Using gitk

1. Run `gitk` in the command line.
2. Look for the commit that you want to find the children of.
3. Right-click on the commit and select "Find Children".
4. The next commit (or commits) will be highlighted.
