---
title: Display the differences between the file in the staging area and its original version using git diff
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To view the git diff on a file in the staging area, use the command `git diff --cached <file>`.
---

**Contents**

[TOC]

### Prerequisites

Before you can view the diff of a file in the staging area, you must first add it to the staging area.

### Add File to Staging Area

To add a file to the staging area, use the `git add` command. For example:

`git add myfile.txt`

This will add the file `myfile.txt` to the staging area.

### View Diff

Once the file is in the staging area, you can view the diff using the `git diff` command. For example:

`git diff --staged myfile.txt`

This will show you the differences between the file in the staging area and the version of the file in the last commit.

### Remove File from Staging Area

If you need to remove the file from the staging area, you can use the `git reset` command. For example:

`git reset myfile.txt`

This will remove the file from the staging area.
