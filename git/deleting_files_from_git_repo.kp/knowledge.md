---
title: What is the process for removing a file from a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To delete a file from a Git repository, use the `git rm` command.
---

**Contents**

[TOC]

### Step 1: Remove the File From the Working Tree

In order to delete a file from a Git repository, you must first remove the file from the working tree. This can be done by running the following command:

`git rm <file_name>`

### Step 2: Commit the Change

Once the file has been removed from the working tree, you must commit the change in order to permanently delete the file from the repository. This can be done by running the following command:

`git commit -m "Removed <file_name>"`

### Step 3: Push the Change

Finally, you must push the change to the remote repository in order for the file to be deleted from the Git repository. This can be done by running the following command:

`git push origin <branch_name>`
