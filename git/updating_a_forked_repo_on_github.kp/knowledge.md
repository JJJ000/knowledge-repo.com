---
title: How can I keep my forked repository on github up to date?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To update or sync a forked repository on GitHub, you can pull in upstream changes from the original repository using git pull.
---

**Contents**

[TOC]

### 1. Fetch the remote branches

When you fork a repository on GitHub, you create a copy of the original repository (upstream repository) with your GitHub username as the owner. This copy acts as a remote repository where you can make changes and commit them. To sync your forked repository with the upstream repository, you need to fetch the remote branches from the upstream repository.

### 2. Add the upstream repository

In order to fetch the remote branches from the upstream repository, you need to add the upstream repository as a remote to your local repository. This can be done by running the following command in the terminal:

```shell
git remote add upstream <url-of-upstream-repository>
```

### 3. Pull the changes

Once you have added the upstream repository, you can pull the changes from the upstream repository by running the following command:

```shell
git pull upstream <branch-name>
```

### 4. Push the changes

Finally, you can push the changes to your forked repository on GitHub by running the following command:

```shell
git push origin <branch-name>
```
