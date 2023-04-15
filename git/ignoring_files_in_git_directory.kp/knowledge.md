---
title: What is the process for excluding files from a directory when using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use a `.gitignore` file to specify which files and directories should be ignored by Git.
---

**Contents**

[TOC]

### Gitignore

Gitignore is a file that contains a list of files and folders that should be ignored by Git. It is used to prevent certain files from being tracked by Git.

### Creating a .gitignore file

1. Create a file named “.gitignore” in the root directory of your project.
2. Add the files and/or folders you want to ignore to the .gitignore file.
3. Save the file.

### Ignoring files in a directory

1. Create a new directory in the root of your project.
2. Add the files you want to ignore to the new directory.
3. Add the directory name to the .gitignore file.

### Adding Multiple Patterns

You can also add multiple patterns to the .gitignore file, separated by a new line. For example, if you want to ignore all files in a directory named “temp” and all files with the extension “.log”, you could add the following to the .gitignore file:

```
temp/
*.log
```
