---
title: What is the process for preventing git from monitoring and disregarding modifications to a file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To stop tracking and ignore changes to a file in Git, use the `git update-index --assume-unchanged <file>` command.
---

**Contents**

[TOC]

### Step 1: Unstage the File

First, you need to unstage the file. This can be done by running the following command:

`git reset HEAD <file>`

This will unstage the file and stop tracking any changes made to it.

### Step 2: Ignore the File

Next, you need to tell Git to ignore any changes made to the file. This can be done by adding the file to the `.gitignore` file. If the `.gitignore` file does not exist, you can create it in the root directory of your repository.

### Step 3: Commit the Changes

Finally, you need to commit the changes. This can be done by running the following command:

`git commit -m "Ignore <file>"`

This will commit the changes and ensure that the file is ignored and not tracked.
