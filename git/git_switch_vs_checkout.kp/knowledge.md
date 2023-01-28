---
title: What is the distinction between git switch and git checkout <branch>?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git switch is used to switch branches and create a new branch, while git checkout is used to switch to an existing branch.
---

**Contents**

[TOC]

### Difference in Syntax
Git switch is written as `git switch <branch>` and git checkout is written as `git checkout <branch>`.

### Difference in Functionality
Git switch is a new command introduced in Git version 2.23 that allows users to switch branches. Git checkout, on the other hand, is a more generic command that can be used to switch branches, create branches, and more.

### Difference in Workflow
Git switch is designed to make it easier to switch between branches. It will automatically create a new branch if the specified branch does not exist. Git checkout, on the other hand, requires users to explicitly create a new branch before they can switch to it.

### Difference in Error Handling
Git switch will throw an error if the specified branch does not exist. Git checkout, however, will not throw an error, and will instead create a new branch with the specified name.
