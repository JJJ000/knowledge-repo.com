---
title: What is the command to view all commits that altered a particular file?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To list all commits that changed a specific file in Git, use the command `git log <file-name>`.
---

**Contents**

[TOC]

### Checkout the File
1. First, you need to checkout the file you want to list commits for. To do this, use the `git checkout` command with the file path as an argument:

```git
git checkout <file path>
```

### List Commits
2. Next, you can use the `git log` command to list all commits that have changed the file. This command takes the `--follow` flag, which will show all commits that have changed the file, even if it has been renamed or moved:

```git
git log --follow <file path>
```

### Limit Output
3. You can also limit the output of the `git log` command to show only the commits that have changed the file. To do this, use the `--name-only` flag:

```git
git log --follow --name-only <file path>
```

### Format Output
4. Finally, you can format the output of the `git log` command to make it easier to read. To do this, use the `--pretty` flag with the `format` option:

```git
git log --follow --name-only --pretty=format:"%h %an %ad %s" <file path>
```

This will format the output to show the commit hash, author name, commit date, and commit message.
