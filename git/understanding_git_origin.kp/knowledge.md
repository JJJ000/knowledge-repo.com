---
title: What does "origin" refer to in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: In Git, `origin` is the default remote repository that is used to push and pull changes from.
---

**Contents**

[TOC]

### Definition

Origin is a reference to a remote repository. It is typically created when you clone a repository from a remote source, and is considered to be the 'default' remote repository that you pull from and push to.

### Usage

When you clone a repository from a remote source, Git automatically creates a remote connection called "origin" that points back to the cloned repository. This allows you to push and pull changes between the local repository and the remote repository.

### Configuration

The origin remote can be configured to point to a different repository, or multiple repositories, by running the `git remote add` command. This is useful if you want to push and pull changes from multiple remote repositories.

### Aliases

The origin remote is often referred to as "upstream" or "upstream remote". This is a common alias used to refer to the remote repository that you pull changes from and push changes to.
