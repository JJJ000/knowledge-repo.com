---
title: How can I remove a file from git without deleting it from my computer?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the `git rm --cached` command to remove a file from your Git repository without deleting it from disk.
---

**Contents**

[TOC]

### Option 1: Move the File

1. Navigate to the directory containing the file you wish to remove from git.
2. Move the file to another directory outside of the git repository.
3. Run the command `git rm <file_name>` to remove the file from the git repository.

### Option 2: Create a .gitignore File

1. Navigate to the directory containing the file you wish to remove from git.
2. Create a `.gitignore` file in the repository.
3. Add the file name to the `.gitignore` file.
4. Run the command `git rm --cached <file_name>` to remove the file from the git repository.
