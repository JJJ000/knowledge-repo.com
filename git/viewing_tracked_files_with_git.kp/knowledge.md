---
title: What command can I use to display a list of files that are being tracked by git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run the command `git ls-files` to show a list of the files that are being tracked.
---

**Contents**

[TOC]

#Section 1: List All Tracked Files

1. Open the terminal.
2. Change directory to the project root.
3. Enter the following command: `git ls-tree --full-tree -r HEAD`

#Section 2: List Tracked Files in a Subdirectory

1. Open the terminal.
2. Change directory to the project root.
3. Enter the following command: `git ls-tree --full-tree -r HEAD <subdirectory>`

#Section 3: List Modified Files

1. Open the terminal.
2. Change directory to the project root.
3. Enter the following command: `git ls-files --modified`

#Section 4: List Untracked Files

1. Open the terminal.
2. Change directory to the project root.
3. Enter the following command: `git ls-files --others --exclude-standard`
