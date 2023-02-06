---
title: What is the command to view a git log in reverse order?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `--reverse` flag when running the git log command.
---

**Contents**

[TOC]

# Section 1: Using 'git log'

The `git log` command is used to view the history of a repository. By default, `git log` will display the commits in chronological order, from the most recent to the oldest.

# Section 2: Reversing the Order

To view the commits in reverse order, you can use the `--reverse` flag. This will display the commits from oldest to newest.

# Section 3: Example

For example, to view the commits in reverse order, you can use the following command:

```
git log --reverse
```

# Section 4: Other Options

In addition to the `--reverse` flag, you can also use the `-n` flag to limit the number of commits displayed. For example, to view the last 5 commits in reverse order, you can use the following command:

```
git log -n 5 --reverse
```
