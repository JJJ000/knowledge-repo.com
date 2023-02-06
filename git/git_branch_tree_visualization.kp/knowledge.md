---
title: Display git branches in a hierarchical tree structure
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git branch can be displayed in a tree-like fashion using the `-vv` flag to show the branch hierarchy.
---

**Contents**

[TOC]

# Section 1: Overview

Git branch is a command used to list, create, or delete branches. It is used to switch between branches in a repository.

# Section 2: Syntax

The syntax for the git branch command is as follows:

```
git branch [--list] [--create] [--delete] [<branch_name>]
```

# Section 3: Tree Like Fashion

The git branch command can be used to display branches in a tree-like fashion. To do this, use the `--list` flag:

```
git branch --list
```

This will display all branches in the repository in a tree-like fashion, with the currently active branch indicated by an asterisk (*).

# Section 4: Example

For example, if you have the following branches in a repository:

- master
- feature-1
- feature-2

Running the command `git branch --list` will display the following output:

```
* master
  feature-1
  feature-2
```
