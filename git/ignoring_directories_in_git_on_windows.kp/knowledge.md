---
title: Excluding directories from git repositories on windows
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To ignore directories in Git repositories on Windows, use the .gitignore file.
---

**Contents**

[TOC]

### Excluding Files from Git

Git provides a way to exclude certain files or directories from being tracked by the version control system. This can be useful if you want to keep certain files or directories out of your repository, such as configuration files, build artifacts, or sensitive data.

### Windows

On Windows, you can exclude files or directories by adding a `.gitignore` file to the root of your repository. This file can contain a list of files or directories to be ignored by Git.

### Syntax

The syntax for the `.gitignore` file is fairly straightforward. Each line contains a pattern that matches the files or directories to be ignored. Wildcards can be used to match multiple files or directories.

For example, to ignore all files in the `build` directory, you can use the following pattern:

```
build/*
```

### Example

Here is a sample `.gitignore` file that ignores the `build` directory and all files in the `config` directory:

```
build/*
config/*
```
