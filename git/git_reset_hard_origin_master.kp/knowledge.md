---
title: What does it mean to execute a git reset --hard origin/master?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git reset --hard origin/master is a command that will reset the local repository to match the remote repository, discarding any local changes.
---

**Contents**

[TOC]

### Overview
Git reset --hard origin/master is a command used to reset a local repository to its original state by overwriting all changes in the working directory with the contents of the origin/master branch.

### Purpose
The purpose of this command is to discard all local changes and reset the repository to the exact state of the origin/master branch.

### Usage
This command is typically used when a user needs to discard all local changes and restore the repository to the exact state of the origin/master branch.

### Examples
For example, if a user has made changes to the local repository that they now want to discard, they can use the command git reset --hard origin/master to reset the repository to the exact state of the origin/master branch.
