---
title: What is the function of git-mv?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git-mv is used to move or rename files, directories, and symlinks in a git repository while preserving their version history.
---

**Contents**

[TOC]

### Purpose
Git-mv is a command line tool used for renaming files and directories within a Git repository. It is a part of the Git version control system and can be used to move and/or rename files and directories from one location to another.

### How it Works
Git-mv works by first taking a snapshot of the file or directory that is being moved or renamed. This snapshot is then added to the repository and the new file or directory is created. The old file or directory is then removed from the repository.

### Benefits
Git-mv helps to keep track of changes in the repository and can be used to quickly rename or move files and directories. It also helps to keep the repository organized and makes it easier to find files and directories.

### Limitations
Git-mv does not work with binary files, such as images and videos. It also does not work with files that are larger than 100MB. Additionally, it cannot be used to move or rename files and directories across different repositories.
