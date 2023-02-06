---
title: What determines the value of origin/head?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Origin/HEAD is set in Git when a remote repository is cloned, and it points to the default branch of the remote repository.
---

**Contents**

[TOC]

# Setting origin/HEAD

Origin/HEAD is an alias for the remote branch pointed to by the special remote named "origin". It is used to keep track of the current branch that the remote repository is on.

## Git Fetch

The most common way to set origin/HEAD is by running the `git fetch` command. This command will pull down any changes from the remote repository and update the origin/HEAD pointer to the latest remote branch.

## Git Push

Another way to set origin/HEAD is by running the `git push` command. This command will push any local changes to the remote repository and update the origin/HEAD pointer to the latest local branch.

## Other Methods

In addition to `git fetch` and `git push`, origin/HEAD can also be set by manually editing the `.git/config` file or by running the `git remote set-head` command.
