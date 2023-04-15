---
title: Examining commits that have not been pushed to a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To view unpushed Git commits, use the `git log` command with the `--not --pushed` flag.
---

**Contents**

[TOC]

### 1. Viewing Log

The easiest way to view unpushed commits is to use the `git log` command. This command will display a list of all commits that have been made to the repository, including those that have not been pushed to the remote.

### 2. Filtering Log

By default, `git log` will show all commits. To filter the log to only show unpushed commits, the `--not` flag can be used with the `git log` command. For example, the following command will only show commits that have not been pushed to the remote:

```
git log --not --remotes
```

### 3. Using Branches

Another way to view unpushed commits is to use branches. When creating a new branch, any commits made on the branch will be considered unpushed until they are merged into the main branch. To view the commits that have been made on a branch, the `git log` command can be used with the `-b` flag. For example, to view the commits made on a branch named `my-branch`, the following command can be used:

```
git log -b my-branch
```

### 4. Using Diffs

The `git diff` command can also be used to view unpushed commits. This command will compare two different commits and show the differences between them. This can be used to compare the current commit to the last commit that was pushed to the remote. For example, the following command will compare the current commit to the last commit that was pushed to the remote:

```
git diff HEAD@{1}
```
