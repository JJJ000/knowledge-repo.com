---
title: Is it possible to compare untracked files using git diff?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: No, git diff cannot be used on untracked files.
---

**Contents**

[TOC]

### No

Git diff is a command used to compare two versions of a file or two sets of files. It can compare tracked files that are part of the repository and are tracked by Git, but it cannot compare untracked files.

### What is an Untracked File?

An untracked file is a file that is not part of the repository and is not tracked by Git. These files are not part of the repository and are not tracked by Git, so they cannot be compared using the git diff command.

### What Can I Use Instead?

If you need to compare two untracked files, you can use a different command-line tool such as diff or meld. These tools will compare two files and show the differences between them.
