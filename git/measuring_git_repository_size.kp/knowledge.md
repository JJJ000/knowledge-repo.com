---
title: Determine the size of a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The size of a Git repository is determined by the total size of all its objects.
---

**Contents**

[TOC]

### Storage

Git repositories are stored as files on a computer or server. The size of a Git repository depends on the number of files and the size of each file.

### Data

Git stores data as objects in a database. Each object contains a file's contents, as well as some additional information about the file. The size of a Git repository is determined by the total size of all the objects in the database.

### Commits

Each commit to a Git repository adds new objects to the database. The more commits, the larger the repository.

### Branches

When a branch is created in a Git repository, a copy of the current state of the repository is made. This means that each branch adds objects to the database, which increases the size of the repository.
