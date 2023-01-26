---
title: How to retrieve a remote branch from git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To fetch a remote branch, use the command `git fetch <remote> <branch>`.
---

**Contents**

[TOC]

### What is Git Fetch
Git fetch is a command used to download content from a remote repository. It allows a user to access the latest version of a repository without having to clone the whole repository. It is often used to synchronize a local repository with a remote repository.

### How to Fetch a Remote Branch
To fetch a remote branch, you need to first identify the remote repository from which you want to fetch the branch. Then, you can use the git fetch command to download the branch from the remote repository.

### Examples
For example, if you want to fetch the “master” branch from a remote repository named “origin”, you can use the following command:

```shell
git fetch origin master
```

This will download the “master” branch from the “origin” remote repository and store it in your local repository.

### Updating Your Local Repository
Once you have fetched the remote branch, you can use the git merge command to update your local repository with the changes from the remote branch. This will ensure that your local repository is in sync with the remote repository.
