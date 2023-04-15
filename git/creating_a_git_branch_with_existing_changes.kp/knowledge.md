---
title: Make a git branch containing the current modifications
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Create a new branch with the current changes by running the command `git checkout -b <branch\_name>`.
---

**Contents**

[TOC]

### Step 1: Create a New Branch

In order to create a new branch with the current changes, the first step is to create a new branch from the current branch. This can be done by using the `git branch` command.

```
git branch <new_branch_name>
```

### Step 2: Checkout the New Branch

Once the new branch is created, the next step is to checkout the new branch. This can be done by using the `git checkout` command.

```
git checkout <new_branch_name>
```

### Step 3: Push the New Branch

Once the new branch is checked out, the changes can be pushed to the remote repository. This can be done by using the `git push` command.

```
git push origin <new_branch_name>
```

### Step 4: Merge Changes

Finally, the changes can be merged into the new branch. This can be done by using the `git merge` command.

```
git merge <current_branch>
```
