---
title: How can I transfer some files from one git repository to another, while keeping their commit history intact?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Use `git log --follow` to identify the files to move, then use `git filter-branch` to copy the files with their history to the other repo.
---

**Contents**

[TOC]

### 1. Create a Local Copy of the Repository

First, you need to create a local copy of the existing repository. You can do this by cloning the repository, or by downloading a zip file of the repository.

### 2. Create a New Repository

Next, you need to create a new repository where you can push the files. This can be done on GitHub or any other version control platform.

### 3. Copy the Files to the New Repository

Once you have created the new repository, you can copy the files you want to move from the old repository to the new repository. You can do this manually by copying and pasting the files, or you can use a tool such as `git mv` to move the files and preserve the history.

### 4. Push the Files to the New Repository

Finally, you can push the files to the new repository. This will commit the files to the new repository and preserve the commit history.
