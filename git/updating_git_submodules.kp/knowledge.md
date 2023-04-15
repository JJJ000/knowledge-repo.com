---
title: Run a git submodule update
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git submodule update is used to fetch the latest commits from a submodule`s remote repository and update the submodule`s working tree.
---

**Contents**

[TOC]

### Overview
Git submodule update is a command used to synchronize a submodule's remote reference with the local repository. This command allows users to fetch changes from the remote repository and incorporate them into the local repository. The command also allows users to update the submodule's working tree to match the commit specified in the parent repository.

### Syntax
The syntax for the git submodule update command is as follows:

```
git submodule update [--init] [--remote] [--rebase] [--merge] [--recursive] [--] [<path>...]
```

### Options
The following options are available for the git submodule update command:

* `--init`: Initialize the submodule's working tree.
* `--remote`: Fetch changes from the remote repository and incorporate them into the local repository.
* `--rebase`: Rebase the submodule's working tree onto the commit specified in the parent repository.
* `--merge`: Merge the changes from the remote repository into the local repository.
* `--recursive`: Recursively update any nested submodules.
* `--`: Separator for paths that follow.
* `<path>...`: Paths to the submodules to update.

### Examples
The following example updates the submodule located at `path/to/submodule`:

```
git submodule update path/to/submodule
```

The following example updates all submodules in the repository:

```
git submodule update --recursive
```
