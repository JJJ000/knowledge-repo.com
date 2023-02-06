---
title: Use git diff to display only lines that have been changed
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git diff --unified=0` to show only lines that have been modified.
---

**Contents**

[TOC]

#### git diff -U0
This command will show only the lines that have been modified in a diff output.

#### git diff --name-only
This command will show only the names of the files that have been modified.

#### git diff --stat
This command will show a summary of the changes, such as the number of lines added, removed, and modified.

#### git diff --cached
This command will show the changes that have been staged for commit.
