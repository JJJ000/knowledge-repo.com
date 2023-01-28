---
title: What is the difference between a commit and its parent?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To diff a commit with its parent in Git, use the `git diff <commit>^ <commit>` command.
---

**Contents**

[TOC]

### Checkout the Commit

1. Retrieve the commit hash of the commit you wish to diff.
2. Use the `git checkout` command to checkout the commit.

### Diff the Commit

1. Use the `git diff` command to diff the commit with its parent.

### View the Diff

1. After running the `git diff` command, you will see the diff output in the terminal.

### Exit the Commit

1. After viewing the diff, use the `git checkout` command to exit the commit.
