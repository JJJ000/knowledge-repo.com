---
title: How can I compare the differences between two files located in different branches using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To diff two different files in different branches, use the command `git diff <branch1> <file1> <branch2> <file2>`.
---

**Contents**

[TOC]

### Step 1: Checkout the Branches

To compare two different files in two different branches, you first need to checkout the branches you want to compare. You can do this with the `git checkout` command:

```
git checkout <branch1>
git checkout <branch2>
```

### Step 2: Check the File Paths

Before you can compare the files, you need to make sure you know the exact file paths for each file. You can use the `git ls-tree` command to list the contents of a branch:

```
git ls-tree <branch1>
git ls-tree <branch2>
```

### Step 3: Compare the Files

Once you have the file paths for both files, you can compare them with the `git diff` command:

```
git diff <file1> <file2>
```

This will show you the differences between the two files.

### Step 4: Clean Up

Once you're done comparing the files, you can switch back to your original branch with the `git checkout` command:

```
git checkout <original_branch>
```
