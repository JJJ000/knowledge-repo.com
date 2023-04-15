---
title: What is the distinction between using git stash pop and git stash apply?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Git stash pop removes the most recently stashed changes from the stash and applies them, while git stash apply applies the most recently stashed changes without removing them from the stash.
---

**Contents**

[TOC]

### Git Stash Pop
Git stash pop will remove the most recent stashed item from the stash stack and apply it to the working directory. It is a combination of git stash apply and git stash drop.

### Git Stash Apply
Git stash apply will apply the most recent stashed item from the stash stack to the working directory without removing it from the stash stack.

### Difference
The main difference between git stash pop and git stash apply is that git stash pop will remove the most recent stashed item from the stash stack after applying it to the working directory, while git stash apply will only apply the most recent stashed item from the stash stack to the working directory without removing it from the stash stack.
