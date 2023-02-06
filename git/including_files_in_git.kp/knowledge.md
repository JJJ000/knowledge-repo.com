---
title: Can git be configured to include specific files while ignoring others?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use the `git add` command to specify which files to include in a commit.
---

**Contents**

[TOC]

1. Using the `.gitignore` File

The most common way to tell git to only include certain files is to use the `.gitignore` file. This file contains a list of files and/or directories that should be ignored by git. If a file or directory is listed in the `.gitignore` file, then git will not track changes to that file or directory.

2. Using the `git add` Command

The `git add` command can be used to explicitly add files to the git repository. This command can be used to add only certain files, while ignoring other files. For example, to add all `.txt` files in the current directory, the following command can be used:

```
git add *.txt
```

3. Using the `git update-index` Command

The `git update-index` command can be used to explicitly add files to the git repository, while ignoring other files. This command is similar to the `git add` command, but it has more options for specifying which files should be added and which should be ignored. For example, to add all `.txt` files in the current directory, while ignoring all `.md` files, the following command can be used:

```
git update-index --add *.txt --ignore-removal *.md
```

4. Using the `git commit` Command

The `git commit` command can be used to commit changes to the git repository. This command can be used to specify which files should be included in the commit and which should be ignored. For example, to commit only `.txt` files in the current directory, while ignoring all `.md` files, the following command can be used:

```
git commit -m "My commit message" --include *.txt --ignore *.md
```
