---
title: How to make a 'git commit' for a single file/directory
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To commit a single file or directory, use the command `git commit <file/directory>`.
---

**Contents**

[TOC]

### Step 1: Add the File/Directory

To add a single file or directory to the staging area, use the `git add` command followed by the file or directory you want to add:

```
git add <file or directory>
```

### Step 2: Commit the File/Directory

To commit the file or directory to the repository, use the `git commit` command followed by a commit message:

```
git commit -m "<commit message>"
```

### Step 3: Push the File/Directory

To push the file or directory to the remote repository, use the `git push` command:

```
git push
```

### Step 4: Check the Commit

To check that the file or directory has been committed, use the `git log` command to view the commit history:

```
git log
```
