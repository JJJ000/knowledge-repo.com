---
title: Retrieve changes from the remote repository after a forced update using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git pull` to fetch and merge any remote changes that were made after the forced update.
---

**Contents**

[TOC]

### 1. What is Forced Update?
A forced update is when a user pushes new changes to a remote repository that conflicts with the existing changes on the local repository. This can happen when two users push conflicting changes to the same repository, or when a user makes changes on a remote repository that the local repository does not have.

### 2. What is Git Pull?
Git pull is a command used to download the latest version of a repository from a remote server and merge it with the local version. It is a combination of git fetch, which downloads the new data, and git merge, which integrates the new changes into the local version.

### 3. What Happens After a Forced Update?
After a forced update, the local repository will be out of sync with the remote repository. This means that the remote repository has changes that the local repository does not have. To bring the local repository up to date, the user must run a git pull command to download the latest version of the repository from the remote server and merge it with the local version.

### 4. What Should You Do After a Forced Update?
After a forced update, the user should run a git pull command to download the latest version of the repository from the remote server and merge it with the local version. This will ensure that the local repository is up to date with the remote repository and that all changes are properly integrated.
