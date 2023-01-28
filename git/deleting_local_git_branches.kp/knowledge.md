---
title: Remove all git branches stored on the local machine
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git branch -D` followed by the name of each local branch to delete them.
---

**Contents**

[TOC]

**1. Listing Local Branches**

To list all local branches, use the following command:

```
git branch -a
```

**2. Deleting Local Branches**

To delete a local branch, use the following command:

```
git branch -d <branch_name>
```

**3. Deleting Multiple Local Branches**

To delete multiple local branches at once, use the following command:

```
git branch -D $(git branch | grep -v "master")
```

**4. Deleting Remote Branches**

To delete a remote branch, use the following command:

```
git push origin --delete <branch_name>
```
