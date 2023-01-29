---
title: What is the method that git uses to store files?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git stores files in a series of snapshots that represent the changes made to a repository over time.
---

**Contents**

[TOC]

### Section 1 - Git Objects
Git stores all of its data in Git objects. These objects are stored in a .git directory within the project's root directory. There are three types of Git objects: blobs, trees, and commits.

### Section 2 - Blobs
Blobs store the content of a file. When a file is added to a repository, a blob is created. The blob stores the file's content and its SHA-1 hash.

### Section 3 - Trees
Trees are objects that store the directory structure of a repository. They point to blobs and other trees, thus creating a hierarchy of the repository's files and folders.

### Section 4 - Commits
Commits are objects that store a snapshot of the repository at a certain point in time. Each commit contains a pointer to a tree object, a pointer to the parent commit, and the author's name and email address.
