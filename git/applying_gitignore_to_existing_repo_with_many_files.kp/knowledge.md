---
title: Add a .gitignore file to an existing repository that is already tracking a large number of files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can apply a .gitignore file to an existing repository that is already tracking large number of files by adding the .gitignore file to the repository and committing it.
---

**Contents**

[TOC]

### Create a .gitignore File

1. Create a new file in the repository root directory and name it `.gitignore`.
2. Add the file patterns you want to ignore to the `.gitignore` file. 

### Add the .gitignore File to the Repository

1. Add the `.gitignore` file to the repository by running the command `git add .gitignore`.
2. Commit the `.gitignore` file to the repository by running the command `git commit -m "Add .gitignore"`.

### Remove Ignored Files from the Repository

1. Run the command `git rm -r --cached .` to remove all ignored files from the repository.
2. Commit the changes to the repository by running the command `git commit -m "Remove ignored files"`.

### Verify Ignored Files

1. Run the command `git status` to verify that all of the files specified in the `.gitignore` file are now being ignored.
