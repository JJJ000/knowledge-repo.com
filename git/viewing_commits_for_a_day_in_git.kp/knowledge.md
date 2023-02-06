---
title: What are all the commits from a particular day?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can view all commits for a specific day in Git by running the command `git log --oneline --after=`<date>` --before=`<date>``.
---

**Contents**

[TOC]

### Using `git log`

The `git log` command allows you to view commits in a repository. To view all commits for a specific day, you can use the `--since` and `--until` flags. 

For example, to view all commits made on August 1, 2020, you would run the following command:

```
git log --since="2020-08-01 00:00:00" --until="2020-08-01 23:59:59"
```

### Using `git rev-list`

The `git rev-list` command can also be used to view commits in a repository. To view all commits for a specific day, you can use the `--after` and `--before` flags. 

For example, to view all commits made on August 1, 2020, you would run the following command:

```
git rev-list --after="2020-08-01 00:00:00" --before="2020-08-01 23:59:59"
```

### Using `git show`

The `git show` command can be used to view detailed information about a single commit. To view all commits for a specific day, you can use the `--since` and `--until` flags. 

For example, to view all commits made on August 1, 2020, you would run the following command:

```
git show --since="2020-08-01 00:00:00" --until="2020-08-01 23:59:59"
```
