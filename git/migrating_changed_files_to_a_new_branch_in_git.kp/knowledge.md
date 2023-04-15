---
title: Transferring modified files to a different branch for committing
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Switch to the target branch and use the `git add` command to stage the changed files, then use `git commit` to check them in.
---

**Contents**

[TOC]

### 1. Create a New Branch

First, create a new branch to check-in the changed files. This can be done by running the command `git checkout -b <new_branch_name>`.

### 2. Move the Files

Next, move the changed files to the new branch. This can be done by running the command `git mv <file1> <file2> <new_branch_name>`.

### 3. Commit the Changes

Then, commit the changes to the new branch. This can be done by running the command `git commit -m "<message>"`.

### 4. Push the Changes

Finally, push the changes to the new branch. This can be done by running the command `git push <new_branch_name>`.
