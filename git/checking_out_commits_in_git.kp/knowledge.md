---
title: Determine which commit is currently checked out in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The commit currently checked out in Git is the HEAD commit.
---

**Contents**

[TOC]

## Git Log

The easiest way to find out which commit is currently checked out in Git is to use the `git log` command. This command will show the most recent commits in the repository, with the currently checked out commit at the top.

## Git Status

Another way to find out which commit is currently checked out in Git is to use the `git status` command. This command will show the current branch and commit that is checked out.

## Git Reflog

The `git reflog` command can also be used to find out which commit is currently checked out in Git. This command will show a list of all the commits that have been checked out in the repository, with the currently checked out commit at the top.
