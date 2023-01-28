---
title: What is the purpose of the '--set-upstream' command?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: `--set-upstream` creates an association between the current branch and a remote branch, allowing the current branch to push and pull changes to and from the remote branch.
---

**Contents**

[TOC]

### What is '--set-upstream'?

'--set-upstream' is a Git command that allows the local branch to be linked to the remote branch. This command is used when creating a local branch and setting it up to track a remote branch.

### How Does it Work?

The command sets up the local branch to track the remote branch. This allows the local branch to receive updates from the remote branch when changes are made. The command also allows the local branch to push changes to the remote branch. 

### When Should it Be Used?

This command should be used when creating a local branch and setting it up to track a remote branch. This allows the local branch to receive updates from the remote branch and push changes to the remote branch.

### Syntax

The syntax for this command is `git branch --set-upstream-to <remote>/<branch>`. The <remote> is the name of the remote repository and the <branch> is the name of the remote branch.
