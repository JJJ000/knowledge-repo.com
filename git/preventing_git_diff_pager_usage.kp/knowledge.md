---
title: What is the best way to stop 'git diff' from opening a pager?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git --no-pager diff` to prevent git diff from using a pager.
---

**Contents**

[TOC]

### Solution 1

### Using the `--no-pager` Flag

The most straightforward way to prevent `git diff` from using a pager is to use the `--no-pager` flag when running the command. This will ensure that the output of `git diff` will be printed directly to the terminal, rather than being sent to a pager.

For example, the following command will run `git diff` without using a pager:

```git
git diff --no-pager
```

### Solution 2

### Setting the `GIT_PAGER` Environment Variable

Another way to prevent `git diff` from using a pager is to set the `GIT_PAGER` environment variable to an empty string. This will tell git to use an empty string as the default pager for all commands, including `git diff`.

For example, the following command will set the `GIT_PAGER` environment variable to an empty string:

```git
export GIT_PAGER=''
```

Once the `GIT_PAGER` environment variable has been set, all subsequent `git diff` commands will not use a pager.
