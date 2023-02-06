---
title: What is the best way to prevent certain directories/files from appearing in a git grep search?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `-v` option to exclude certain directories/files from git grep search.
---

**Contents**

[TOC]

#### Excluding Files

1. Create a `.gitignore` file in the root directory of the repository.
2. Add the file names or directory paths to be excluded in the `.gitignore` file.
3. Use the `--no-exclude-standard` flag when running `git grep` to make sure the `.gitignore` file is used.

#### Excluding Directories

1. Create a `.git/info/exclude` file in the root directory of the repository.
2. Add the directory paths to be excluded in the `.git/info/exclude` file.
3. Use the `--no-exclude-standard` flag when running `git grep` to make sure the `.git/info/exclude` file is used.
