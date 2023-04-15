---
title: Shift the branch pointer to a different commit without switching branches
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the `git reset` command to move the branch pointer to a different commit without checking it out.
---

**Contents**

[TOC]

### Using Reset

Git provides the `reset` command to move the branch pointer to a different commit. This command can be used to move the branch pointer to a different commit without performing a checkout.

### Syntax

The following command can be used to move the branch pointer to a different commit without checkout:

`git reset --soft <commit>`

### Options

The `--soft` option is used to move the branch pointer without changing the working tree or the staging area.

### Benefits

Using this command, the branch pointer can be moved to a different commit without having to perform a checkout. This can be useful when the goal is to move the branch pointer without changing the working tree or the staging area.
