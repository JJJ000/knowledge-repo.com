---
title: What does "git checkout -- --" mean?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git checkout double dashes is a command used to switch to a specific branch or commit in a repository.
---

**Contents**

[TOC]

### Definition

Git checkout double dashes is a command used to switch between branches in a Git repository. It is used to switch the current branch to another branch, or to restore files in the working tree to a specific commit.

### Syntax

The syntax for using the git checkout double dashes command is as follows:

git checkout -- <branch name>

### Usage

The git checkout double dashes command is used to switch branches in a Git repository. It can also be used to restore files in the working tree to a specific commit.

### Examples

To switch to a branch called “my-branch”:

git checkout -- my-branch

To restore a file to a specific commit:

git checkout -- <commit hash> <file name>
