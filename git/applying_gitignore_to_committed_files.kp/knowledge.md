---
title: Adding a .gitignore to files that have already been committed
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: It is not possible to apply .gitignore to already committed files.
---

**Contents**

[TOC]

### Removing Files from the Repository

It is not possible to remove files from the repository that have already been committed. This is because git stores a snapshot of the entire repository at each commit, and it would be impossible to go back and change the history of the repository.

### Ignoring Committed Files

Although it is not possible to remove files from the repository that have already been committed, it is possible to ignore the committed files. This can be done by adding the file path of the committed files to the `.gitignore` file. This will prevent the committed files from being tracked by git, and they will no longer show up in the repository.

### Adding the .gitignore File

In order to add the `.gitignore` file to the repository, it must first be added to the staging area. This can be done by running the command `git add .gitignore`. After the `.gitignore` file has been added to the staging area, it can be committed to the repository by running the command `git commit -m "Adding .gitignore file"`.

### Verifying the .gitignore File

Once the `.gitignore` file has been committed to the repository, it can be verified by running the command `git status`. This will show any files that are being tracked by git, as well as any files that are being ignored. If the committed files are being ignored, then the `.gitignore` file has been successfully applied to the committed files.
