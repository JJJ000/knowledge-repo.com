---
title: What is the purpose of hard/soft resets in git and why can't they be done by path?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git does not support operations on individual files or paths, only on entire commits.
---

**Contents**

[TOC]

## What is a Hard/Soft Reset
A hard reset is when you reset the current Git branch to a previous commit, discarding any changes made since that commit. A soft reset is when you reset the current Git branch to a previous commit, but keep the changes made since that commit.

## Why Git Can't Do Hard/Soft Resets by Path
1. Git is designed to track changes to files, not paths. A reset requires Git to understand the changes made to a file, not just the path to the file.
2. Doing a reset by path would require Git to track changes to the entire directory tree, not just individual files. This would require a significant increase in complexity and resources.
3. A reset by path would require the user to specify a path for the reset, which would be difficult to do accurately.
