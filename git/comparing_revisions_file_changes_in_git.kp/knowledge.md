---
title: Identifying which files have been altered between two versions
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To show which files have changed between two revisions in Git, use the `git diff` command.
---

**Contents**

[TOC]

### Using `git diff`

The `git diff` command can be used to show which files have changed between two revisions. It takes two arguments: the commit SHA or branch name for the two revisions you want to compare.

For example, to compare the current state of a repository with the state of the repository two commits ago, you could use the following command:

`git diff HEAD~2 HEAD`

This command will show a list of all the files that have been changed between the two commits.

### Using `git log`

The `git log` command can also be used to show which files have changed between two revisions. It takes two arguments: the commit SHA or branch name for the two revisions you want to compare.

For example, to compare the current state of a repository with the state of the repository two commits ago, you could use the following command:

`git log --name-only --oneline HEAD~2 HEAD`

This command will show a list of all the files that have been changed between the two commits, along with the commit messages for each commit.

### Using `git show`

The `git show` command can also be used to show which files have changed between two revisions. It takes two arguments: the commit SHA or branch name for the two revisions you want to compare.

For example, to compare the current state of a repository with the state of the repository two commits ago, you could use the following command:

`git show --name-only HEAD~2 HEAD`

This command will show a list of all the files that have been changed between the two commits.
