---
title: Deleting multiple files from a git repository that have already been erased from the hard drive
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can remove multiple files from a Git repo that have already been deleted from disk by using the `git rm` command with the file paths as arguments.
---

**Contents**

[TOC]

### Step 1: Remove Files from Git

The first step is to remove the files from the Git repository. This can be done by running the following command:

`git rm <filename>`

This command will remove the specified file from the repository. If multiple files need to be removed, the command can be run multiple times with different filenames.

### Step 2: Commit Changes

Once the files have been removed from the repository, the changes need to be committed. This can be done by running the following command:

`git commit -m "Removing <filename>"`

This command will commit the changes to the repository with a message describing what was done.

### Step 3: Push Changes

Once the changes have been committed, they need to be pushed to the remote repository. This can be done by running the following command:

`git push origin <branch_name>`

This command will push the changes to the remote repository.

### Step 4: Clean up

Finally, the local repository needs to be cleaned up. This can be done by running the following command:

`git clean -f`

This command will remove any files that have been deleted from the local repository.
