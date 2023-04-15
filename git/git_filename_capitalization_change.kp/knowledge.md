---
title: Altering the case of file names in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git does not change the capitalization of filenames.
---

**Contents**

[TOC]

### Overview

Git is a popular version control system used by software developers to track changes in the codebase. It is especially useful for tracking changes in filenames. However, when filenames are changed, the capitalization of the filenames may also be changed. It is important to be aware of how Git handles changes in capitalization of filenames.

### How Git Handles Changes in Capitalization

Git considers changes in capitalization of filenames to be a change in the file's content. This means that when a file is renamed with a different capitalization, Git will treat it as a new file and will not recognize it as the same file. This can be problematic if the file is part of a repository and other developers are relying on the file's contents.

### Steps to Preserve Capitalization

To preserve capitalization of filenames in Git, developers should follow these steps:

1. Before making any changes, make sure to commit the original file with the original capitalization.
2. When making changes, use the `-f` flag to force Git to recognize the file as the same one.
3. After making the changes, commit the file again with the new capitalization.

### Conclusion

Preserving capitalization of filenames in Git is important to ensure that all developers are able to access the same version of the file. By following the steps outlined above, developers can ensure that changes in capitalization of filenames are properly tracked in Git.
