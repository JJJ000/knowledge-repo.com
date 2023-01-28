---
title: Handling big binary files with git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git Large File Storage (LFS) can be used to manage large binary files with Git.
---

**Contents**

[TOC]

### Pre-Commit Strategies

In order to manage large binary files with Git, it is important to first consider strategies for minimizing the size of the files before they are committed to the repository. Some strategies for reducing the size of binary files before they are committed include:

1. Compressing the file: Compressing the file with a tool like zip or gzip can often reduce the size of a binary file significantly.

2. Reducing the resolution: If the binary file is an image, reducing the resolution can often reduce the file size significantly.

3. Removing unnecessary data: If the binary file contains unnecessary data, such as metadata or comments, removing this data can reduce the file size.

### Git LFS

Git Large File Storage (LFS) is a Git extension that can be used to manage large binary files. Git LFS tracks large files and stores them on a remote server, rather than storing them in the repository itself. This allows for faster cloning and fetching of repositories, as only the necessary files are downloaded.

### Gitignore

Gitignore is a file that can be used to tell Git which files to ignore when committing to the repository. This can be useful for ignoring large binary files, as they will not be committed to the repository, but can still be stored locally.

### Alternatives

Finally, there are several alternatives to using Git for managing large binary files. For example, services such as Dropbox and Google Drive can be used to store large binary files, and can be integrated with Git for version control. Additionally, there are several services specifically designed for version control of large binary files, such as Perforce and Plastic SCM.
