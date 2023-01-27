---
title: What is the command to see a git log of a single user's commits?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can view a git log of just one user`s commits by using the `--author` option with the git log command.
---

**Contents**

[TOC]

### Using `git log`

The `git log` command allows you to view a log of all commits made in a repository. To view the commits of a single user, you can use the `--author` option.

For example, to view all commits made by a user with the email address `user@example.com`, you can run the following command:

```git
git log --author="user@example.com"
```

### Using `git shortlog`

The `git shortlog` command allows you to view a summarized log of all commits made in a repository. To view the commits of a single user, you can use the `--author` option.

For example, to view all commits made by a user with the email address `user@example.com`, you can run the following command:

```git
git shortlog --author="user@example.com"
```

### Using `git rev-list`

The `git rev-list` command allows you to view a list of all commits made in a repository. To view the commits of a single user, you can use the `--author` option.

For example, to view all commits made by a user with the email address `user@example.com`, you can run the following command:

```git
git rev-list --author="user@example.com"
```

### Using `git log --format`

The `git log --format` command allows you to view a customized log of all commits made in a repository. To view the commits of a single user, you can use the `--author` option.

For example, to view all commits made by a user with the email address `user@example.com`, you can run the following command:

```git
git log --format="%H %an %ae" --author="user@example.com"
```

This command will output a list of all commit hashes, author names, and email addresses for the specified user.
