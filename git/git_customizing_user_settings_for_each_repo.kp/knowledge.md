---
title: Set a different local user.name and user.email for each git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, it is possible to set local user.name and user.email for each repo by using the `git config` command.
---

**Contents**

[TOC]

### Setting Local User.Name

1. Change directory to the root of the repository: `cd /path/to/repo`
2. Set the local user.name of the repository: `git config user.name "Your Name"`

### Setting Local User.Email

1. Change directory to the root of the repository: `cd /path/to/repo`
2. Set the local user.email of the repository: `git config user.email "your@email.com"`

### Verifying the Settings

1. Change directory to the root of the repository: `cd /path/to/repo`
2. Check the local user.name and user.email settings of the repository: `git config --list`

### Setting Global User.Name and User.Email

1. Set the global user.name and user.email: `git config --global user.name "Your Name"` and `git config --global user.email "your@email.com"`
