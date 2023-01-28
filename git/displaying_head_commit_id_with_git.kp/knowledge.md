---
title: What is the git command to show the id of the head commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The command to display the HEAD commit id is `git rev-parse HEAD`.
---

**Contents**

[TOC]

#1 Git show

The `git show` command can be used to display the HEAD commit id.

#2 Syntax

The syntax for `git show` is:

`git show [options] [<object>]`

#3 Options

The `-s` option can be used to display the abbreviated commit hash.

#4 Example

The following command displays the HEAD commit id:

`git show -s HEAD`
