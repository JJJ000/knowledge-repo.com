---
title: What steps do I need to take to undo any changes I have made that have not been committed, including files and folders?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the `git reset --hard` command to revert uncommitted changes including files and folders in Git.
---

**Contents**

[TOC]

### Using `git reset`

`git reset` is a powerful command that can be used to undo commits, reset the index and working tree, and even unstage files. To revert uncommitted changes, use the `--hard` flag.

```git
git reset --hard
```

This command will discard any changes that have been made to the working tree and index since the last commit.

### Using `git checkout`

`git checkout` can be used to revert changes to a single file or folder. To revert a single file, use the following command:

```git
git checkout <file_name>
```

To revert a folder, use the `--` flag:

```git
git checkout -- <folder_name>
```

### Using `git clean`

`git clean` can be used to remove untracked files and directories from the working tree. This command is useful for cleaning up any files or folders that were created but not added to the repository.

```git
git clean -f
```

The `-f` flag will force the removal of untracked files and folders.
