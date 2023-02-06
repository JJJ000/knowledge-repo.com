---
title: What is the easiest way to omit typing "git" when executing git commands?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can set up an alias for the Git command, such as `g` instead of `git`.
---

**Contents**

[TOC]

## Set Up an Alias
One way to avoid typing `git` at the beginning of every Git command is to set up an alias. An alias is a way of creating a shortcut for a command. To set up an alias for `git`, open your terminal and type the following command:

```
$ alias g='git'
```

This will create a shortcut for the `git` command. From now on, you can use `g` instead of `git` when typing Git commands.

## Add Alias to Bash Profile
In order for the alias to persist after closing and reopening your terminal, you can add the alias to your Bash profile. To do this, open your Bash profile in a text editor:

```
$ nano ~/.bash_profile
```

Then, add the alias to the bottom of the file:

```
alias g='git'
```

Save the file and close the text editor. The alias will now persist after closing and reopening your terminal.

## Use a Git-Specific Terminal
Another way to avoid typing `git` at the beginning of every Git command is to use a terminal specifically designed for Git. A Git-specific terminal will automatically recognize `git` commands and will not require you to type `git` at the beginning of every command.
