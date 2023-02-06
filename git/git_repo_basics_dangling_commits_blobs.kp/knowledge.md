---
title: What are dangling commits and blobs in a git repository, and how do they originate?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A dangling commit is a commit that is not reachable from any branch or tag, and a blob is a type of object in a Git repository that stores the contents of a file; they both come from commits that have been made in the repository.
---

**Contents**

[TOC]

### Dangling Commit

A dangling commit is a commit in a Git repository that is not reachable from any branch or tag. It is typically the result of a failed operation such as a rebase or a failed merge. Dangling commits can be identified by running the command `git fsck --unreachable`.

### Blob

A blob is a data object in a Git repository that stores file data. Blobs are created when a file is added to the repository and are identified by a hash of the file contents. Blobs can be accessed through the command `git cat-file -p <hash>`.
