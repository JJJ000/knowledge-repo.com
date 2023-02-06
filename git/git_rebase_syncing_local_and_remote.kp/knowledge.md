---
title: Track changes to the local and remote versions of a repository using git rebase
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git rebase is used to move a branch onto the latest commit of a remote branch, while keeping track of the local and remote branches.
---

**Contents**

[TOC]

### Rebase

Rebasing is a way to combine multiple commits into a single commit. It can be used to keep a local branch in sync with a remote branch.

### Local

When rebasing, the local branch is the branch that is being rebased. It is the branch that will have its commits rebased onto the remote branch.

### Remote

The remote branch is the branch that the local branch is being rebased onto. It is the branch that will receive the new commits from the local branch.

### Keeping Track

In order to keep track of the local and remote branches during a rebase, it is important to be aware of which branch is the local and which is the remote. The local branch should always be the one that is being rebased, and the remote should be the one that is receiving the new commits. Additionally, it is important to keep track of the order in which commits are being rebased, so that any conflicts can be resolved quickly and efficiently.
