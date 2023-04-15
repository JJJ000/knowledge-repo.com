---
title: Use 'git mv' to rename a directory and only alter its casing
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can use `git mv` to only change the case of a directory.
---

**Contents**

[TOC]

### Renaming Directories with Git Mv

### Overview
Git mv is a Git command that allows users to move or rename a file, directory, or a symlink. It is the equivalent of the Unix mv command, but with the added benefit of version control.

### Changing Case of Directory
When using the Git mv command, it is possible to only change the case of a directory without changing its name.

### Syntax
The syntax for using Git mv to change the case of a directory is as follows:

```
git mv <old_directory> <new_directory>
```

Where `<old_directory>` is the current name of the directory, and `<new_directory>` is the new case-changed version of the directory.

### Example
For example, if the directory `MyDirectory` needs to be changed to `mydirectory`, the command would be:

```
git mv MyDirectory mydirectory
```
