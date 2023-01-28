---
title: What is the process for altering the remote that a branch is linked to?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To change the remote a branch is tracking in Git, use the command `git branch -u <remote>/<branch>`.
---

**Contents**

[TOC]

### Step 1: List All Remotes

To see what remote branches are currently being tracked, you can use the `git remote -v` command. This will list all remotes and their associated URLs.

### Step 2: Change the Remote

You can use the `git remote set-url` command to change the remote a branch is tracking. The syntax for this command is `git remote set-url <remote_name> <url>`.

### Step 3: Verify the Change

To verify the change, you can use the `git remote -v` command again. This will show the updated remote and its associated URL.

### Step 4: Push the Changes

Finally, you can use the `git push` command to push the changes to the remote. This will update the remote with the new URL.
