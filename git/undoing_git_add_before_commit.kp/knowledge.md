---
title: What is the procedure for reversing a 'git add' before committing?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: You can undo a git add before a commit by using the command `git reset`.
---

**Contents**

[TOC]

### Undoing with 'git reset'

The most straightforward way to undo a 'git add' before a commit is to use the `git reset` command. This command will unstage all changes that have been added to the index.

### Syntax

The syntax for the `git reset` command is as follows:

```shell
git reset <file>
```

Where <file> is the file that you want to unstage.

### Unstaging Multiple Files

If you want to unstage multiple files, you can use the `git reset` command with the `--mixed` flag. This flag will unstage all changes that have been added to the index.

The syntax for the `git reset` command with the `--mixed` flag is as follows:

```shell
git reset --mixed
```

### Unstaging All Files

If you want to unstage all changes that have been added to the index, you can use the `git reset` command with the `--hard` flag. This flag will unstage all changes that have been added to the index, as well as resetting any changes that have been made to the working tree.

The syntax for the `git reset` command with the `--hard` flag is as follows:

```shell
git reset --hard
```
