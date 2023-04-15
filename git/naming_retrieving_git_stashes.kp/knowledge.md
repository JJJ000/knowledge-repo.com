---
title: What is the process for assigning a name to a git stash and retrieving it later using that name?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can name a Git stash with the command `git stash save <name>` and retrieve it by name with the command `git stash apply <name>`.
---

**Contents**

[TOC]

### Naming a Git Stash

To name a Git stash, you can use the `git stash save` command with the `--name` flag. For example, to name a stash "my-stash", you can use the command `git stash save --name my-stash`.

### Retrieving a Git Stash by Name

To retrieve a Git stash by name, you can use the `git stash apply` command with the `--name` flag. For example, to retrieve the stash named "my-stash", you can use the command `git stash apply --name my-stash`.
