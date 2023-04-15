---
title: How can I turn a local git repository into a remote one?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Create a remote repository on a hosting service such as GitHub, GitLab, or Bitbucket and push the local repository to it.
---

**Contents**

[TOC]

### Initialize a Local Repository
1. Create a folder on your local machine to store the project files.
2. In the folder, initialize a local Git repository with the `git init` command.

### Create a Remote Repository
1. Create a remote repository on your preferred hosting service (e.g. GitHub, Bitbucket, etc.).
2. Copy the remote repository's URL.

### Link the Local Repository to the Remote Repository
1. In the local repository, add the remote repository with the `git remote add` command.
2. Paste the remote repository's URL as the argument for the command.

### Push the Local Repository to the Remote Repository
1. Push the local repository to the remote repository with the `git push` command.
2. Enter the remote repository's URL as the argument for the command.
