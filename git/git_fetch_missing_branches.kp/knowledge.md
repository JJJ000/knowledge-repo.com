---
title: Git's 'fetch' command does not retrieve all branches
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git fetch only downloads the data from the remote repository, but it does not automatically update any of the local branches.
---

**Contents**

[TOC]

### What is Fetch in Git?
Fetch is a Git command used to download objects and refs from a remote repository. Fetching is an essential operation in Git and is used to keep the local repository up-to-date with the remote repository. It is also used to retrieve branches and commits from the remote repository.

### Does Fetch Get All Branches?
No, fetching in Git does not get all branches. When you fetch in Git, it only downloads the content from the remote repository that is specified in the command. It does not download all the branches from the remote repository.

### How to Fetch All Branches?
In order to fetch all branches from a remote repository, you need to use the git fetch command with the --all or -a flag. This flag will tell Git to fetch all branches from the remote repository.

### Summary
Fetching in Git is an essential operation used to keep the local repository up-to-date with the remote repository. However, fetching does not get all branches from the remote repository. To fetch all branches from the remote repository, you need to use the git fetch command with the --all or -a flag.
