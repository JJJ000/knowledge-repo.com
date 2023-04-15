---
title: What is the command to find the root directory of a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Yes, the command `git rev-parse --show-toplevel` can be used to get the git root directory.
---

**Contents**

[TOC]

### Solution 1

Using the `git rev-parse` command, you can get the git root directory by running the following command:

```git
git rev-parse --show-toplevel
```

### Solution 2

Another way to get the git root directory is to use the `git rev-parse` command with the `--git-dir` option:

```git
git rev-parse --git-dir
```

This command will output the path to the .git directory, which is located in the root directory of the repository.

### Solution 3

You can also use the `git rev-parse` command with the `--show-cdup` option:

```git
git rev-parse --show-cdup
```

This command will output the relative path from the current directory to the root directory of the repository.

### Solution 4

Finally, you can use the `git rev-parse` command with the `--show-prefix` option:

```git
git rev-parse --show-prefix
```

This command will output the relative path from the root directory of the repository to the current directory.
