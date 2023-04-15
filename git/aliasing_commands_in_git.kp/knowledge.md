---
title: What is the process for creating an alias for a command in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can alias commands in git by using the `git config --global alias.alias\_name command` command.
---

**Contents**

[TOC]

### Step 1: Create an Alias

To create an alias, use the `git config` command. For example, to create an alias for the `git status` command, type the following command into the terminal:

`git config --global alias.st status`

The `--global` flag sets the alias in your global configuration so that it is available in all repositories.

### Step 2: Use the Alias

To use the alias, simply type the alias name instead of the full command. For example, to use the `git status` alias created in the previous step, type the following command:

`git st`

### Step 3: List Aliases

To list all of your aliases, use the `git config --get-regexp alias` command.

### Step 4: Remove an Alias

To remove an alias, use the `git config --global --unset alias.<alias_name>` command. For example, to remove the `git status` alias created in the first step, type the following command:

`git config --global --unset alias.st`
