---
title: Find the total number of commits made by each author across all branches in a git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The number of commits per author on all branches can be determined by running the git shortlog command.
---

**Contents**

[TOC]

`**` Counting Commits on All Branches**

To count the number of commits per author on all branches, you can use the `git shortlog` command. This command will show the number of commits and the authors who made them on all branches.

For example, to get the number of commits per author on the master branch, you can run the following command:

`git shortlog -s -n master`

This will show the number of commits and the authors who made them on the master branch.

`**` Counting Commits on Specific Branches**

You can also count the number of commits per author on specific branches. To do this, you can use the `git log` command.

For example, to get the number of commits per author on the feature/my-feature branch, you can run the following command:

`git log --author="<author_name>" --oneline --decorate --graph feature/my-feature`

This will show the number of commits and the authors who made them on the feature/my-feature branch.

`**` Counting Commits Across Multiple Branches**

You can also count the number of commits per author across multiple branches. To do this, you can use the `git log` command with the `--all` flag.

For example, to get the number of commits per author across all branches, you can run the following command:

`git log --author="<author_name>" --oneline --decorate --graph --all`

This will show the number of commits and the authors who made them across all branches.

`**` Counting Commits Across All Branches**

Finally, you can also count the number of commits per author across all branches. To do this, you can use the `git shortlog` command with the `--all` flag.

For example, to get the number of commits per author across all branches, you can run the following command:

`git shortlog -s -n --all`

This will show the number of commits and the authors who made them across all branches.
