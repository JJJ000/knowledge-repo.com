---
title: What are the branches that include a specific commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the command `git branch --contains <commit>` to list branches that contain a given commit in Git.
---

**Contents**

[TOC]

### Install Git

Before you can list branches that contain a given commit in Git, you must first install Git. To install Git, follow the instructions for your operating system here: [https://git-scm.com/book/en/v2/Getting-Started-Installing-Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

### Find the Commit

Once you have Git installed, you can find the commit you are looking for. You can use the `git log` command to list all commits in the current branch. To find a specific commit, you can use the `--grep` option to search for a specific commit message or author.

### List the Branches

Once you have found the commit, you can use the `git branch` command to list all branches that contain the commit. You can use the `--contains` option to filter the results to only display branches that contain the commit.

### Verify the Commit

Finally, you can use the `git show` command to view the commit. This will allow you to verify that the commit is in the branch. You can also use the `--oneline` option to view the commit in a condensed format.
