---
title: Copy a file with git while preserving its history
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To copy a file while preserving its history, use the `git log` command followed by `git checkout` to copy it to a new location.
---

**Contents**

[TOC]

# Section 1: Copying the File

To copy a file and preserve its history, the `git-cp` command can be used. This command works similar to the `cp` command, but preserves the history of the file.

# Section 2: Using git-cp

The `git-cp` command takes two arguments: the source file and the destination file. The command will then copy the source file to the destination while preserving its history.

For example, to copy a file from the current directory to a subdirectory, the following command can be used:

`git-cp file.txt subdir/file.txt`

# Section 3: Viewing File History

After copying the file with `git-cp`, its history can be viewed with the `git log` command. This will show the commits associated with the file, along with the date, author, and commit message.

# Section 4: Further Reading

For more information on using `git-cp` to copy files and preserve their history, please refer to the official Git documentation.
