---
title: I cannot upload to github because I previously had a large file which I have now deleted
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You should try performing a git push --force.
---

**Contents**

[TOC]

### Solution 1: Git LFS

Git Large File Storage (LFS) is an open-source extension to Git that allows users to store large files in a more efficient way. Git LFS works by replacing large files in the repository with small text pointers that reference the large files stored on a remote server. This allows for faster downloads and smaller repositories.

### Solution 2: Git Shrink

Git Shrink is a tool for reducing the size of a Git repository by removing unnecessary files and compressing large files. It also provides additional features such as removing empty directories and optimizing the repository structure.

### Solution 3: Git Bundles

Git Bundles is a feature of Git that allows users to package up a repository into a single file that can be easily shared. This allows users to easily transfer large repositories without having to push them to a remote server.

### Solution 4: Git Large File Transfer

Git Large File Transfer (Git LFT) is a tool for transferring large files between Git repositories. It works by transferring large files in chunks, allowing for faster downloads and smaller repositories.
