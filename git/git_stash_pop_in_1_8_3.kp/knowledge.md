---
title: How can I use git stash pop to retrieve a specific stash in version 1.8.3?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git stash pop <stash\_name>` to pop a specific stash in Git 1.8.3.
---

**Contents**

[TOC]

### Understanding Stashing

Git stash pop is a command used to remove a specific stash from the stack of stashed changes. It is used when you need to apply a specific set of changes from the stash stack and discard the rest.

### Git Stash Pop Syntax

The syntax for the git stash pop command is as follows:

`git stash pop [<stash>]`

Where <stash> is an optional parameter used to specify the stash to be removed from the stack. If no parameter is specified, the command will remove the most recent stash from the stack.

### Git Stash Pop in 1.8.3

In Git version 1.8.3, the git stash pop command works the same way as in newer versions. The only difference is that the command does not accept the --index option, which allows you to apply specific changes from the stash stack.

### Examples

To remove the most recent stash from the stack:

`git stash pop`

To remove a specific stash from the stack:

`git stash pop <stash>`
