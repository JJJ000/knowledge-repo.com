---
title: What is the command to use 'git diff' on a specific directory?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git diff <directory\_name>` to diff a certain directory.
---

**Contents**

[TOC]

1. Setting up the Directory 
    - Navigate to the directory you want to diff. 
    - Execute the command `git diff` in the directory.

2. Using the `--` Option
    - To diff a certain directory, use the `--` option after the command. 
    - For example, `git diff -- <directory>` 

3. Using the `*.` Wildcard 
    - To diff all files in a directory, use the `*.` wildcard after the command. 
    - For example, `git diff *.` 

4. Using the `**` Wildcard 
    - To diff all files in a directory and its subdirectories, use the `**` wildcard after the command. 
    - For example, `git diff **`
