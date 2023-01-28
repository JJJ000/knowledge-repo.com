---
title: Git show only "untracked" files (plus, custom commands)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To list only untracked files, use the command `git ls-files --others --exclude-standard`.
---

**Contents**

[TOC]

### Listing Untracked Files

To list only untracked files in Git, you can use the command `git ls-files --others --exclude-standard`. This command will list all untracked files in the current working directory, excluding any files that are already tracked by Git.

### Custom Commands

In addition to the standard Git commands, users can also create custom commands to facilitate their workflow. Custom commands are created by writing a shell script and adding it to the `$PATH` environment variable. This allows the command to be executed from anywhere in the terminal.

### Examples

For example, a user can create a custom command to list all untracked files in the current working directory. This can be done by creating a shell script that contains the command `git ls-files --others --exclude-standard`. The script should then be placed in the `$PATH` environment variable, allowing the user to execute the command from anywhere in the terminal.

### Benefits

Creating custom commands can be beneficial for users who frequently use the same Git commands. By creating custom commands, users can save time by not having to type out the entire command each time it is needed. Additionally, custom commands can be used to automate repetitive tasks, making the process of using Git more efficient.
