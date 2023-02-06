---
title: Using git version control, committing changes to only a file's permissions
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To update and commit only a file`s permissions using git version control, use the command `git update-index --chmod=+x <file>`.
---

**Contents**

[TOC]

# Section 1: Configure File Permissions

1. Determine the desired permissions for the file.
2. Open a command prompt or terminal window.
3. Navigate to the directory containing the file.
4. Execute the command `chmod [mode] [file]`, where `[mode]` is the permissions mode, and `[file]` is the file to modify.

# Section 2: Stage the File

1. Open a command prompt or terminal window.
2. Navigate to the directory containing the file.
3. Execute the command `git add [file]`, where `[file]` is the file to stage.

# Section 3: Commit the File

1. Open a command prompt or terminal window.
2. Navigate to the directory containing the file.
3. Execute the command `git commit -m "[message]"`, where `[message]` is the commit message.

# Section 4: Push the Commit

1. Open a command prompt or terminal window.
2. Navigate to the directory containing the file.
3. Execute the command `git push origin master`, which will push the commit to the remote repository.
