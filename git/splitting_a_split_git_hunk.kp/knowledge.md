---
title: Is it possible to divide an already divided portion of code using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use the `git add -p` command to split an already split hunk.
---

**Contents**

[TOC]

## Yes

Git allows you to split an already split hunk. To do this, use the `git add -p` command. This command will bring up the patch selection menu, which will allow you to select an already split hunk. From there, you can select the `e` option to edit the hunk and split it further.

## Steps

1. Use the `git add -p` command to bring up the patch selection menu.
2. Select the hunk you want to split.
3. Select the `e` option to edit the hunk.
4. Use the `s` option to split the hunk into smaller hunks.
5. Select the `y` option to accept the split hunks.
