---
title: What are the steps to set file execute mode permissions in git on windows?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: In Git on Windows, you can set file execute mode permissions using the `git update-index --chmod=+x <file>` command.
---

**Contents**

[TOC]

### Setting Up Git
1. Download and install Git on your Windows computer.
2. Create a local repository in the directory where you will store your project files.
3. Open the command prompt and navigate to the local repository.

### Setting File Execute Mode Permissions
1. Use the `git config` command to set the execute mode permissions for the files in the repository.
2. The command should look like this: `git config core.filemode true`.
3. This will set the execute mode permissions for all files in the repository.

### Testing the Execute Mode Permissions
1. Create a test file in the repository and add some code to it.
2. Use the `git status` command to check the execute mode permissions of the file.
3. If the execute mode permissions are set correctly, the output should show the execute mode permissions for the file.

### Committing the Changes
1. Use the `git add` command to add the file to the staging area.
2. Use the `git commit` command to commit the changes to the repository.
3. Use the `git push` command to push the changes to the remote repository.
