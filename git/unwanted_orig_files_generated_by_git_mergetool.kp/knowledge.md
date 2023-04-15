---
title: Git mergetool creates files with the .orig extension that are not desired
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git mergetool can generate unwanted .orig files if the tool is configured to do so.
---

**Contents**

[TOC]

### Solution

### Overview
Git mergetool can generate unwanted .orig files when resolving merge conflicts. These files are created as a backup of the original version of the file before the merge conflict was resolved.

### What are .orig files?
.orig files are backup files created by Git mergetool when resolving merge conflicts. They contain the original version of the file before the conflict was resolved.

### How to prevent .orig files from being created
To prevent .orig files from being created, you can use the `--no-backup` flag when running `git mergetool`. This flag will stop Git from creating backup files.

### Conclusion
Git mergetool can generate unwanted .orig files when resolving merge conflicts. To prevent this from happening, you can use the `--no-backup` flag when running `git mergetool`.
