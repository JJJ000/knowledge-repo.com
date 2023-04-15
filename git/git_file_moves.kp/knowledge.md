---
title: How can I use git to track a file that has been moved to a different location?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `git mv` command to move a file.
---

**Contents**

[TOC]

### Configure Git
1. Open the terminal and navigate to the directory where the files are stored.
2. Run the command `git config --global core.trustctime false` to configure Git to track file moves.

### Add and Commit Files
1. Run the command `git add -A` to add all the files in the directory.
2. Run the command `git commit -m "message"` to commit the changes.

### Move the File
1. Run the command `git mv <old_file> <new_file>` to move the file.
2. Run the command `git commit -m "message"` to commit the changes.

### Push the Changes
1. Run the command `git push origin <branch_name>` to push the changes to the remote repository.
