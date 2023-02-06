---
title: Can git display the number of lines added, modified, and deleted?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use the `git diff --stat` command to show lines added, changed, and removed.
---

**Contents**

[TOC]

#### Using `git diff`

The `git diff` command can be used to show the lines that have been added, changed, and removed.

To show the lines that have been added, use the `--unified=0` flag when running `git diff`. This will output a list of lines that have been added.

To show the lines that have been changed, use the `--unified=1` flag when running `git diff`. This will output a list of lines that have been changed.

To show the lines that have been removed, use the `--unified=2` flag when running `git diff`. This will output a list of lines that have been removed.

#### Using `git log`

The `git log` command can also be used to show the lines that have been added, changed, and removed.

To show the lines that have been added, use the `--name-status` flag when running `git log`. This will output a list of lines that have been added.

To show the lines that have been changed, use the `--name-status` flag and the `--diff-filter=M` flag when running `git log`. This will output a list of lines that have been changed.

To show the lines that have been removed, use the `--name-status` flag and the `--diff-filter=D` flag when running `git log`. This will output a list of lines that have been removed.
