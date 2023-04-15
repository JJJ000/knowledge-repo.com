---
title: How to take a file out of a git repository without erasing it from the local file system?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Run `git rm --cached <file>` to remove the file from the Git repository without deleting it from the local filesystem.
---

**Contents**

[TOC]

### 1. Remove the File From the Repository

To remove a file from a Git repository without deleting it from the local filesystem, you can use the `git rm` command. This command will remove the file from the repository, but will not delete it from your local filesystem.

### 2. Commit the Change

Once the file has been removed from the repository, you will need to commit the change. This can be done with the `git commit` command.

### 3. Push the Change

Once the change has been committed, it will need to be pushed to the remote repository. This can be done with the `git push` command.

### 4. Verify the Change

The final step is to verify that the change has been successfully pushed to the remote repository. This can be done by checking the repository online or by running the `git status` command.
