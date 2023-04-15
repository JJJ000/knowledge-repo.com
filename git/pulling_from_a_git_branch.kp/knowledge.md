---
title: Retrieving changes from a particular branch in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To pull from a specific branch, use the command `git pull <remote> <branch>`.
---

**Contents**

[TOC]

### Pulling from a Specific Branch

When pulling from a remote repository, it is possible to specify which branch to pull from. This can be done using the `git pull` command with the `-b` option.

### Syntax

The syntax for pulling from a specific branch is as follows:

```
git pull <remote_name> <branch_name>
```

Where `<remote_name>` is the name of the remote repository and `<branch_name>` is the name of the branch to pull from.

### Example

For example, to pull from the `master` branch of the `origin` remote repository, the command would be:

```
git pull origin master
```

### Pulling Multiple Branches

It is also possible to pull from multiple branches at once by specifying each branch name after the `-b` option. For example, to pull from the `master` and `develop` branches of the `origin` remote repository, the command would be:

```
git pull origin -b master -b develop
```
