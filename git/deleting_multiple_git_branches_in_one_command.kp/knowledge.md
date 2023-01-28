---
title: Is it possible to delete multiple branches simultaneously using a single git command?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Yes, you can delete multiple branches in one command with Git using the command `git branch -d <branch\_name1> <branch\_name2>...`.
---

**Contents**

[TOC]

Yes

`__Method 1:__`
Using the `git branch -d` command

The `git branch -d` command allows you to delete multiple branches in one command. For example, to delete branches `branch1`, `branch2`, and `branch3` you would use the command:

```
git branch -d branch1 branch2 branch3
```

`__Method 2:__`
Using the `git branch -D` command

The `git branch -D` command allows you to delete multiple branches in one command, even if the branches have not been merged into the current branch. This is useful if you want to quickly delete multiple branches without having to manually merge each one. For example, to delete branches `branch1`, `branch2`, and `branch3` you would use the command:

```
git branch -D branch1 branch2 branch3
```
