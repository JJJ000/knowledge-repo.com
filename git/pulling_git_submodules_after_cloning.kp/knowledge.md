---
title: After cloning a project from github, run the command 'git submodule update --init --recursive' to pull the submodules
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git submodule update --init --recursive` to pull git submodules after cloning a project from GitHub.
---

**Contents**

[TOC]

## Initialize Submodules

To initialize the submodules after cloning the project from GitHub, run the following command in the root directory of the project:

```
git submodule init
```

## Update Submodules

To update the submodules after cloning the project from GitHub, run the following command in the root directory of the project:

```
git submodule update
```

## Verify Submodules

To verify that the submodules have been initialized and updated correctly, run the following command in the root directory of the project:

```
git submodule status
```

This command should list all of the submodules and their current commit hashes.
