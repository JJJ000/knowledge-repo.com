---
title: Undo the addition of a file in the most recent commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the `git reset HEAD~1` command to remove a file from the latest commit in Git.
---

**Contents**

[TOC]

### Removing a File from the Latest Commit

### Step 1: Check Out the Commit

The first step in removing a file from the latest commit is to check out the commit. This can be done using the `git checkout` command.

### Step 2: Remove the File

Once the commit has been checked out, the file can be removed using the `git rm` command. This will remove the file from the repository and the commit.

### Step 3: Commit the Changes

Once the file has been removed, the changes need to be committed. This can be done using the `git commit` command.

### Step 4: Push the Changes

Finally, the changes need to be pushed to the remote repository. This can be done using the `git push` command.
