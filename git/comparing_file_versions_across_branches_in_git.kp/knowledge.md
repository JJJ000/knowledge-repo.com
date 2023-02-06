---
title: Compare the current version of a file with the version of the same file committed to a different branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To diff the current working copy of a file with another branch`s committed copy in Git, use the `git diff <branch> <file>` command.
---

**Contents**

[TOC]

# Section 1: View Differences

To view the differences between a file in the current working copy and a file in another branch's committed copy, you can use the `git diff` command.

# Section 2: Syntax

The syntax for using `git diff` is:

```
git diff <branch1> <branch2> -- <file>
```

Where `<branch1>` is the branch containing the file in the current working copy, `<branch2>` is the branch containing the committed copy of the file, and `<file>` is the path to the file.

# Section 3: Example

For example, to view the differences between a file in the current working copy and a file in the `master` branch, the command would be:

```
git diff HEAD master -- <file>
```

# Section 4: Output

The output of the command will be a list of the differences between the two files.
