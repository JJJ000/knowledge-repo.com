---
title: Retrieve a list of commits between two tags in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git log <tag1>..<tag2>` to get the commit list between two tags.
---

**Contents**

[TOC]

### Using git log

1. Open the terminal window
2. Navigate to the local repository with `cd [repository_name]`
3. Enter the command `git log [tag1]..[tag2]` to get a list of commits between two tags

### Using git rev-list

1. Open the terminal window
2. Navigate to the local repository with `cd [repository_name]`
3. Enter the command `git rev-list [tag1]..[tag2]` to get a list of commits between two tags

### Using git tag

1. Open the terminal window
2. Navigate to the local repository with `cd [repository_name]`
3. Enter the command `git tag --list [tag1]..[tag2]` to get a list of commits between two tags
