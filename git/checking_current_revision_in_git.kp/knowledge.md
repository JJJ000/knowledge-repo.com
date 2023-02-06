---
title: What is my current revision number in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can view the current revision of your repository by running the command `git rev-parse HEAD`.
---

**Contents**

[TOC]

#Git Log

One way to figure out what your current revision is in Git is to use the `git log` command. This command will show you a list of all the commits that have been made to the repository. Each commit is identified by its unique SHA-1 hash, which is a 40-character string that is used to identify the commit.

#Git Status

Another way to figure out what your current revision is in Git is to use the `git status` command. This command will show you the current branch that you are on, as well as the SHA-1 hash of the most recent commit on that branch.

#Git Show

A third way to figure out what your current revision is in Git is to use the `git show` command. This command will show you the contents of the most recent commit on the current branch. It will also include the SHA-1 hash of the commit, which can be used to identify the commit.
