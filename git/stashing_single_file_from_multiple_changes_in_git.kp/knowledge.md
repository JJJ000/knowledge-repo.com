---
title: What is the process for saving only one of the multiple modified files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Run `git stash push -m <message> -- <file>` to stash only one file out of multiple files that have changed.
---

**Contents**

[TOC]

### 1. Stage the File

First, you must stage the file that you want to stash. This is done using the `git add` command.

```shell
git add <file_name>
```

### 2. Check the Status

Next, you should check the status of your repository to make sure that the file you want to stash is the only one that has been staged.

```shell
git status
```

### 3. Stash the File

Once you have verified that only the desired file is staged, you can now stash the file.

```shell
git stash
```

### 4. Verify the Stash

Finally, you should verify that the file has been successfully stashed by checking the list of stashes.

```shell
git stash list
```
