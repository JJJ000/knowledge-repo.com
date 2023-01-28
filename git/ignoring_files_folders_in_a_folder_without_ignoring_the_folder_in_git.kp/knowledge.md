---
title: What is the best way to ignore all the contents of a folder, but not the folder itself, using .gitignore?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use a `.gitignore` file in the folder with a wildcard pattern (`*`) to ignore all files and folders in the folder, but not the folder itself.
---

**Contents**

[TOC]

### Create a .gitignore File

1. Create a file called `.gitignore` in the directory you want to ignore.

### Add Rules to the .gitignore File

2. Add the following rule to the `.gitignore` file:

```git
/*
!.gitignore
```

This rule will ignore all files and folders in the directory, but not the `.gitignore` file itself.

### Commit the .gitignore File

3. Commit the `.gitignore` file to the repository.

### Verify the Ignored Files

4. Verify that the files and folders in the directory are being ignored by running the `git status` command. If the files and folders are being ignored, they will not be listed in the output of the command.
