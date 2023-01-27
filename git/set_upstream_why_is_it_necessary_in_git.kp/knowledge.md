---
title: What is the purpose of running "--set-upstream" frequently?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: `--set-upstream` is used to link the local branch to a remote repository so that changes can be pushed and pulled.
---

**Contents**

[TOC]

### What is '--set-upstream'?

`--set-upstream` is a command used in Git to set the upstream repository for a local branch. This command tells Git which remote repository the local branch should be tracking.

### Why is it Necessary?

In order to ensure that changes made to the local branch are properly tracked, it is necessary to set the upstream repository. This allows the user to push their changes to the remote repository and pull any changes made by other users.

### When is it Necessary?

It is necessary to use `--set-upstream` whenever a new local branch is created. It is also necessary to use `--set-upstream` if the upstream repository for a local branch has been changed.

### How to Do it?

The command `git push --set-upstream <remote> <branch>` can be used to set the upstream repository for a local branch. The <remote> argument should be the name of the remote repository and the <branch> argument should be the name of the local branch.
