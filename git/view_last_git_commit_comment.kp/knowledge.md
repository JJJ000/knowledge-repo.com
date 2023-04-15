---
title: Show the most recent git commit message
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The last git commit comment can be displayed by running the command `git log -1`.
---

**Contents**

[TOC]

### Using Git Log

The following command can be used to view the last git commit message:

`git log -1 --pretty=format:"%s"`

This will output the commit message of the last commit.

### Using Git Show

The following command can be used to view the last git commit message:

`git show -s --format=%B`

This will output the commit message of the last commit.

### Using Git Reflog

The following command can be used to view the last git commit message:

`git reflog --format="%s" -1`

This will output the commit message of the last commit.

### Using Git Describe

The following command can be used to view the last git commit message:

`git describe --always --abbrev=0 --tags`

This will output the commit message of the last commit.
