---
title: How can I create a new local branch, push it to a remote git repository, and track it?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To push a new local branch to a remote Git repository and track it, use the command `git push -u origin <branch-name>`.
---

**Contents**

[TOC]

### Create Local Branch
1. Checkout a new local branch from the desired starting point:
```shell
git checkout -b <branch_name> <start_point>
```
2. Make changes and commit them to the new local branch:
```shell
git add <file_name>
git commit -m "<commit_message>"
```

### Push Local Branch to Remote
1. Push the new local branch to the remote repository:
```shell
git push -u origin <branch_name>
```
2. Check the remote to make sure the branch was pushed successfully:
```shell
git remote -v
```

### Track Branch
1. Set the local branch to track the remote branch:
```shell
git branch --set-upstream-to=origin/<branch_name> <branch_name>
```
2. Check the status of the branch tracking:
```shell
git branch -vv
```
