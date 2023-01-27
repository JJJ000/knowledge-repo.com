---
title: Do not consider files that have been added to a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git will ignore files that have already been committed to the repository.
---

**Contents**

[TOC]

1. Exclude Files from Git Tracking
--------------------------------

Git allows you to exclude files from being tracked by adding them to the `.gitignore` file. This file is located in the root of your repository and contains a list of files and/or directories that should not be tracked by Git. When you commit changes, Git will check the `.gitignore` file and will not commit any files that match the patterns in the file.

2. Use the `git rm` Command
---------------------------

If you have already committed a file to the repository, you can use the `git rm` command to remove the file from the repository. This will delete the file from the repository and will not track it in the future.

3. Use the `git update-index` Command
------------------------------------

The `git update-index` command allows you to mark a file as “assume-unchanged”. This will tell Git to ignore any changes to the file, even if it has already been committed to the repository.

4. Use the `git reset` Command
-----------------------------

The `git reset` command can be used to undo a commit and remove the file from the repository. This is useful if you want to remove a file from the repository without deleting it from your local system.
