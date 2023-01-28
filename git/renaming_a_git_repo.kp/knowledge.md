---
title: What is the procedure for changing the name of a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run the command `git remote set-url <new-url> <old-url>` to rename a Git repository.
---

**Contents**

[TOC]

1. **Find the Repository in the Command Line**

Open the command line and navigate to the directory that contains the repository you want to rename.

2. **Rename the Repository**

Run the following command to rename the repository:

`git mv <old-name> <new-name>`

3. **Update the Remote Repository**

If the repository is connected to a remote repository, you need to update the remote repository with the new name. To do this, run the following command:

`git remote set-url origin <new-url>`

4. **Verify the Rename**

To verify that the repository has been renamed, run the following command:

`git remote -v`

This will list the remote repositories associated with the repository. The new repository name should be listed.
