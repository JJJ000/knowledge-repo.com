---
title: Excluding all files and directories except those specified in the .gitignore file
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a .gitignore file that includes a line to ignore all files and directories, followed by lines to explicitly include the desired directories.
---

**Contents**

[TOC]

# Method 1
1. Create a `.gitignore` file in the root of your repository.
2. Add the following line to `.gitignore`:
```
*
```
3. Create a `.git/info/exclude` file in the root of your repository.
4. Add the following lines to `.git/info/exclude`:
```
!*/
!directory_name_1/
!directory_name_2/
```

# Method 2
1. Create a `.gitignore` file in the root of your repository.
2. Add the following lines to `.gitignore`:
```
*
!directory_name_1/
!directory_name_2/
```
3. Create a `.git/info/exclude` file in the root of your repository.
4. Add the following line to `.git/info/exclude`:
```
!*/
```
