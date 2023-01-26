---
title: What is the best way to delete untracked files from my current git working tree?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To remove local (untracked) files from the current Git working tree, use the `git clean` command.
---

**Contents**

[TOC]

### Using git clean

1. To remove all untracked files from the current working tree, use the `git clean` command with the `-f` flag:

```shell
git clean -f
```

2. To remove all untracked files and directories from the current working tree, use the `-d` flag:

```shell
git clean -fd
```

### Using find and rm

1. To remove all untracked files from the current working tree, use the `find` and `rm` commands:

```shell
find . -not -path ‘*/\.*’ -type f -exec rm -f {} \;
```

2. To remove all untracked files and directories from the current working tree, use the `-type d` flag:

```shell
find . -not -path ‘*/\.*’ -type d -exec rm -rf {} \;
```
