---
title: What is the command to stage and commit all files, including newly added ones, at once?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the command `git add -A && git commit -m <message>` to stage and commit all files, including newly added files, in one command.
---

**Contents**

[TOC]

### Using `git add`

The `git add` command can be used to stage all files, including newly added files, in a single command. By running `git add .`, you can stage all files in the current directory, including new and modified files.

### Using `git commit`

Once the files have been staged, you can use the `git commit` command to commit them all in one command. To do this, you can use the `-a` flag with the `git commit` command, which will automatically stage all modified and deleted files before committing.

### Using `git commit -a`

You can combine the `git add` and `git commit` commands into a single command by using the `git commit -a` command. This command will automatically stage all modified and deleted files before committing them.

### Using `git commit -am`

The `git commit -am` command can be used to stage and commit all files, including newly added files, in a single command. This command will automatically stage all modified and deleted files, as well as any new files, before committing them.
