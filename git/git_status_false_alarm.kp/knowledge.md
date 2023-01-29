---
title: Git status indicates that files have been altered even though their contents remain the same
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git compares files based on their content`s checksums, so even small differences in the file can be detected.
---

**Contents**

[TOC]

### Checking File Differences
Git is designed to detect any changes to a file, including changes in content, file name, and permissions. It does this by comparing the file's checksum, which is a unique identifier for the file. If the checksum is different, the file is considered to have changed.

### Ignoring Whitespace
Git can also be configured to ignore whitespace when checking for changes. This means that even if two files have the same content, but different whitespace, Git will not detect a difference. This can be useful when working with certain programming languages, as whitespace is often insignificant.

### Configuring Git
Git can be configured to ignore changes to certain files or folders. This can be done by adding a `.gitignore` file to the repository, which contains a list of files and folders to ignore. This can be useful if there are files which are regularly changed, but don't need to be tracked by Git.

### Summary
Git status can show files as changed even if the contents are the same. This is because Git compares the file's checksum to detect changes. It can also be configured to ignore whitespace, or to ignore certain files or folders.
