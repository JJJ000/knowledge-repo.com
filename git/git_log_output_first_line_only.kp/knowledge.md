---
title: What is the command to show only the first line of the git log?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `--oneline` flag with the `git log` command.
---

**Contents**

[TOC]

### Using `--oneline`

Git provides the `--oneline` flag for the `git log` command, which can be used to output only the first line of the log.

### Syntax

The syntax for the command is as follows:

```git
git log --oneline
```

### Example

For example, the following command outputs only the first line of the log:

```git
git log --oneline
```

The output will be similar to this:

```git
f3b8a1d (HEAD -> master, origin/master, origin/HEAD) Add README.md
```

### Additional Flags

In addition to the `--oneline` flag, there are other flags that can be used to customize the output of the `git log` command, such as `--graph` and `--decorate`. For more information about these flags and how to use them, see the [Git Documentation](https://git-scm.com/docs/git-log).
