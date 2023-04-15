---
title: Create a .gitignore file that excludes all files except for the specified few
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Create a .gitignore file that contains the paths of the files you want to keep track of.
---

**Contents**

[TOC]

### Exclude Everything

Add the following line to the `.gitignore` file:

```git
*
```

This will exclude all files and folders from being tracked by Git.

### Include Specific Files

To include specific files, add the following lines to the `.gitignore` file:

```git
!.gitignore
!file1.txt
!file2.txt
```

This will allow Git to track the `.gitignore` file, as well as `file1.txt` and `file2.txt`.

### Include Specific Folders

To include specific folders, add the following lines to the `.gitignore` file:

```git
!folder1/
!folder2/
```

This will allow Git to track all the files and subfolders in the `folder1` and `folder2` folders.

### Exclude Specific Files

To exclude specific files, add the following lines to the `.gitignore` file:

```git
*.txt
!file1.txt
!file2.txt
```

This will exclude all `.txt` files except `file1.txt` and `file2.txt`.
