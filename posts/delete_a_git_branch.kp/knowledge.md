---
title: How do I delete a Git branch?
authors:
- cool_wizard
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use `git branch -d <branch_name>` to delete a local branch,
  or `git push origin --delete <branch_name>` to delte a remote branch.
---

**Contents**

[TOC]

### Delete a local Git branch

To delete a Git branch locally, use the following command:

```shell
git branch -d <branch_name>
```

This will delete the branch locally. If you want to force delete the branch, even if it has unmerged changes, use the `-D` option instead of `-d`.

```shell
git branch -D <branch_name>
```

### Delete a remote Git branch

To delete the branch remotely, use the following command:

```shell
git push origin --delete <branch_name>
```

This will delete the branch from the remote repository. If you want to delete the branch from a different remote, replace origin with the name of the remote.

### Delete a Git branch both locally and remotely

You can also delete the branch locally and remotely at the same time by using the `-d` option with `git push`:

```shell
git push origin -d <branch_name>
```

This will delete the branch both locally and remotely. If you want to force delete the branch, use the `-D` option instead of `-d`.

```shell
git push origin -D <branch_name>
```

Keep in mind that deleting a branch is a permanent action and cannot be undone. Make sure you really want to delete the branch before running these commands.
