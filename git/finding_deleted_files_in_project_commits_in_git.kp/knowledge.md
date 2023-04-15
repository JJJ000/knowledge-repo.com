---
title: What steps can I take to locate a file that has been removed from the project's commit history?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To find a deleted file in the project commit history in Git, use the command `git log --diff-filter=D --summary`.
---

**Contents**

[TOC]

### Overview

Git is a version control system that allows us to track changes made to our codebase over time. It can be used to find deleted files in the project commit history. This guide will explain how to find a deleted file in the project commit history in Git.

### Step 1: Check the Git Log

The first step is to check the Git log. This can be done by running the command `git log --diff-filter=D --summary`. This will show a list of all the deleted files in the project commit history.

### Step 2: Check the Commit Message

The next step is to check the commit message for each deleted file. This can be done by running the command `git show [commit-hash]` where [commit-hash] is the commit hash associated with the deleted file. This will show the commit message, which may contain information about why the file was deleted.

### Step 3: Check the Previous Commits

Finally, you can check the previous commits to see if the deleted file was modified before it was deleted. This can be done by running the command `git log --follow [file-name]`. This will show the list of commits that modified the file before it was deleted.
