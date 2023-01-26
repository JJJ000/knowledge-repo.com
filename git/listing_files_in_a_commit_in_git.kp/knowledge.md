---
title: What is the command to show all the files included in a commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Use the command `git show --name-only --oneline` to list all the files in a commit in Git.
---

**Contents**

[TOC]

### Using Git Log

The `git log` command can be used to list all files in a commit. It will display the commit hash, author, date, and message for each commit. To view the files associated with a particular commit, use the `--name-only` or `--name-status` flags.

For example, to list all files associated with the most recent commit, you can use the following command:

```shell
git log --name-only -1
```

### Using Git Show

The `git show` command can be used to view the contents of a particular commit. It displays the commit hash, author, date, message, and a list of all files associated with the commit.

For example, to view the contents of the most recent commit, you can use the following command:

```shell
git show
```

### Using Git Diff

The `git diff` command can be used to view the differences between two commits. It will display the list of files that have been modified or added between the two commits.

For example, to view the differences between the most recent commit and the previous commit, you can use the following command:

```shell
git diff HEAD^ HEAD
```
