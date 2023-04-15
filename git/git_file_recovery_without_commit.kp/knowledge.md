---
title: Retrieve a file that was deleted without any commits made afterwards using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: It is not possible to recover a deleted file if no commit was made after the delete.
---

**Contents**

[TOC]

### Check the Trash
The easiest way to recover a deleted file that has not been committed to a repository is to check the trash or recycle bin of the computer. Depending on the operating system, the deleted file may be in the trash or recycle bin.

### Check the Commit Log
If the file was committed to the repository before it was deleted, then it may be possible to recover the file by checking the commit log. This can be done by running the `git log` command, which will display a list of all the commits that have been made to the repository. From this list, the user can find the commit that contains the deleted file, and then use the `git checkout` command to restore the deleted file.

### Use a Data Recovery Tool
If the file was not committed to the repository before it was deleted, then a data recovery tool may be able to help. There are many data recovery tools available, both free and paid, that can scan a computer's hard drive and attempt to recover deleted files.

### Contact the System Administrator
If all else fails, it may be necessary to contact the system administrator for help. The system administrator may be able to use specialized tools to recover the deleted file.
