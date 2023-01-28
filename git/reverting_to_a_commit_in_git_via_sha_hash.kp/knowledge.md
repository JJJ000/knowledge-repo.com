---
title: How do I go back to a specific commit using its sha hash in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To revert to a commit by a SHA hash in Git, use the command `git revert <SHA hash>`.
---

**Contents**

[TOC]

### Using the Command Line
1. Ensure you are in the correct local repository.
2. Use the `git log` command to find the SHA hash of the commit you want to revert to.
3. Use the `git reset` command to reset the repository to the commit you want to revert to.

### Using a GUI
1. Ensure you are in the correct local repository.
2. Use the GUI to view the commit history and find the SHA hash of the commit you want to revert to.
3. Use the GUI to reset the repository to the commit you want to revert to.
