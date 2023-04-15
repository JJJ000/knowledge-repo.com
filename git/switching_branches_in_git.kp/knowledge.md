---
title: Switch the branch's foundation
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To change the branch base in Git, use the command `git checkout <branch\_name>`.
---

**Contents**

[TOC]

### Step 1: Check Out a New Branch

1. Use the `git checkout` command to create a new branch:

```git
git checkout -b <branch_name>
```

2. This command will create a new branch and switch you to the new branch.

### Step 2: Switch to the Existing Branch

1. Use the `git checkout` command to switch to the existing branch:

```git
git checkout <existing_branch_name>
```

2. This command will switch you to the existing branch.

### Step 3: Set the New Branch as the Base

1. Use the `git branch` command to set the new branch as the base:

```git
git branch --set-upstream-to=<new_branch_name> <existing_branch_name>
```

2. This command will set the new branch as the base for the existing branch.

### Step 4: Push the Changes

1. Use the `git push` command to push the changes to the remote repository:

```git
git push -u origin <existing_branch_name>
```

2. This command will push the changes to the remote repository.
