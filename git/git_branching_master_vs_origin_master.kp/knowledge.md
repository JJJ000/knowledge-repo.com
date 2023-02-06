---
title: What is the difference between 'master', 'origin/master', and 'remotes/origin/master' in git branching?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Master is a local branch, origin/master is a remote tracking branch, and remotes/origin/master is a shorthand for the same remote tracking branch.
---

**Contents**

[TOC]

## Master

The `master` branch is the main branch of the repository. It is the default branch that is created when a new repository is initialized. It is the branch that is typically used for production-ready code.

## Origin/Master

The `origin/master` branch is a remote branch that is created when a repository is cloned from a remote repository. It is a local copy of the remote `master` branch. It tracks the remote `master` branch and is used to keep the local repository up-to-date with the remote repository.

## Remotes/Origin/Master

The `remotes/origin/master` branch is a pointer to the `origin/master` branch. It is used to quickly access the `origin/master` branch. It is not a branch itself, but rather a pointer to the `origin/master` branch.
