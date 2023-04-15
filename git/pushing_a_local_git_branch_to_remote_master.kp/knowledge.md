---
title: What is the process for pushing a local git branch to the master branch on the remote?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To push a local Git branch to the remote master branch, use the command `git push origin <branch\_name>`.
---

**Contents**

[TOC]

### 1. Create a Local Branch

The first step is to create a local branch. This can be done by using the `git checkout` command.

```
git checkout -b <branch_name>
```

This will create a new branch with the specified name and switch to that branch.

### 2. Commit Changes

Once the local branch is created, make the necessary changes to the files and commit them to the local branch.

```
git add <file_name>
git commit -m "Commit message"
```

### 3. Push Branch to Remote

Once the changes have been committed to the local branch, push the branch to the remote repository.

```
git push -u origin <branch_name>
```

### 4. Merge Branch to Master

Finally, merge the local branch to the master branch in the remote repository.

```
git checkout master
git merge <branch_name>
git push origin master
```
