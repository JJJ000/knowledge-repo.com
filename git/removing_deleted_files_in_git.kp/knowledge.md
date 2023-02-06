---
title: How to undo multiple deleted files in a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git gc --prune=now` to remove multiple deleted files in a Git repository.
---

**Contents**

[TOC]

# Section 1: Using `git filter-branch`

The `git filter-branch` command can be used to remove multiple deleted files from a Git repository. This command rewrites the commits in the repository's history, allowing you to make changes to the repository.

# Section 2: Preparing to Use `git filter-branch`

Before using `git filter-branch`, it is important to create a backup of the repository. This can be done by using the `git clone` command to create a copy of the repository.

# Section 3: Using `git filter-branch`

Once the repository has been backed up, `git filter-branch` can be used to remove multiple deleted files. This command takes the following syntax:

```
git filter-branch --tree-filter 'rm -rf <file_name>' --prune-empty HEAD
```

This command will remove the file specified by `<file_name>` from the repository's history.

# Section 4: Finalizing the Process

After using `git filter-branch` to remove multiple deleted files, it is important to clean up the repository. This can be done by running the `git gc` command, which will optimize the repository and remove any unnecessary files.
