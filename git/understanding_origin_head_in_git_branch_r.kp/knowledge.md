---
title: What does 'origin/head' signify when using the command 'git branch -r'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Origin/HEAD is shown when running `git branch -r` because it is the default branch of the remote repository.
---

**Contents**

[TOC]

## What is origin/HEAD?
Origin/HEAD is a reference to the current branch on the remote repository. It is used to track the remote branch that is currently checked out.

## What Does "git branch -r" Do?
The command "git branch -r" lists all the remote branches of the repository. It shows the local branches and the remote branches that are tracked by the local repository.

## Why is origin/HEAD Shown?
Origin/HEAD is shown because it is a reference to the current branch on the remote repository. This allows the user to easily identify which branch is currently checked out in the remote repository.

## Conclusion
Origin/HEAD is shown when running "git branch -r" because it is a reference to the current branch on the remote repository. This allows the user to easily identify which branch is currently checked out in the remote repository.
