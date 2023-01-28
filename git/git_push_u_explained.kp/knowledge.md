---
title: What is the meaning of the command 'git push -u'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git push -u sets the upstream branch for the current branch in your local repository and pushes the changes to the remote repository.
---

**Contents**

[TOC]

### Definition
Git push -u is a command used to push a set of commits to a remote repository and set the upstream branch.

### Usage
This command is used to push a local branch to a remote repository, and set the upstream branch for the local branch. This command is often used to set the upstream branch for the first time when creating a new branch.

### Syntax
The syntax for the command is as follows:

`git push -u <remote> <branch>`

### Example
For example, if you wanted to push a local branch ‘my-branch’ to a remote repository ‘origin’, you would type the following command:

`git push -u origin my-branch`
