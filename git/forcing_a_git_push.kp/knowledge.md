---
title: What is the correct way to perform a git push?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To force a Git push, use the `--force` or `-f` flag when pushing.
---

**Contents**

[TOC]

### Step 1: Add Your Changes

Before you can push your changes to the remote repository, you must first add the changes to the local repository. To do this, use the command `git add <file>` to add the files you have modified.

### Step 2: Commit Your Changes

Once you have added the changes, you must commit them to the local repository. To do this, use the command `git commit -m "<message>"` to commit your changes with a message for future reference.

### Step 3: Push to the Remote Repository

Now that your changes have been committed to the local repository, you can push them to the remote repository. To do this, use the command `git push -f <remote> <branch>` to force the push.

### Step 4: Verify the Push

Finally, you should verify that the push was successful. To do this, use the command `git status` to check the status of the remote repository. If the changes have been successfully pushed, the output should indicate that the remote repository is up to date.
