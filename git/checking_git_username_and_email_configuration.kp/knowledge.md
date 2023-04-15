---
title: What is the git username and email that were set during configuration?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The git username and email saved during configuration can be viewed by running the command `git config --list`.
---

**Contents**

[TOC]

### Section 1 - Check the git config

The git username and email can be found by running the following command:

`git config --list`

This will output all the git configuration settings, including the username and email.

### Section 2 - Check the Global Config File

The git username and email can also be found in the global config file. This file is located in the user's home directory and is named `.gitconfig`.

### Section 3 - Check the Local Config File

The git username and email can also be found in the local config file. This file is located in the repository's directory and is named `.git/config`.

### Section 4 - Check the Command Line

The git username and email can also be found by running the following command:

`git config user.name`

`git config user.email`
