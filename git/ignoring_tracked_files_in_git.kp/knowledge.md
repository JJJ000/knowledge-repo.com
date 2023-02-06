---
title: Exclude tracked files from git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can ignore tracked files by adding them to your .gitignore file.
---

**Contents**

[TOC]

## Unstage files

If you want to ignore changes to an already tracked file, you can unstage it. This can be done using the `git reset HEAD <file>` command. This command will unstage the file and any changes made to it will no longer be tracked by Git.

## Remove files

Another way to ignore changes to a tracked file is to remove the file from the repository. This can be done using the `git rm <file>` command. This will remove the file from the repository and any changes made to it will no longer be tracked by Git.

## Ignore files

You can also tell Git to ignore certain files by adding them to a `.gitignore` file. This file should be located in the root directory of the repository. Any files listed in the `.gitignore` file will be ignored by Git and any changes made to them will not be tracked.

## Using a branch

Finally, you can use branches to ignore changes to tracked files. This can be done by creating a new branch and committing any changes to the tracked files to that branch. The changes will only be tracked in the new branch and will not be tracked in the main branch.
