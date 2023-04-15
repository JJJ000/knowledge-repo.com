---
title: Display the submodules within a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To list submodules in a Git repository, use the command `git submodule status`.
---

**Contents**

[TOC]

### List Submodules

To list the submodules in a Git repository, use the command `git submodule`.

### View Submodule Information

To view information about a specific submodule, use the command `git submodule <submodule-name>`.

### Update Submodules

To update the submodules in a Git repository, use the command `git submodule update --init --recursive`.

### Remove Submodules

To remove a submodule from a Git repository, use the command `git submodule deinit <submodule-name>` followed by `git rm <submodule-name>`.
