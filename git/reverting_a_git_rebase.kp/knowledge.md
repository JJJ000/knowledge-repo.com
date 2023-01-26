---
title: How to revert a git rebase?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To undo a git rebase, run `git rebase --abort`.
---

**Contents**

[TOC]

### Step 1: Reset the Head Pointer

To undo a git rebase, the first step is to reset the head pointer. This can be done by running the following command:

```shell
git reset --hard HEAD~1
```

This command will reset the head pointer to the commit before the rebase began.

### Step 2: Checkout the Rebased Branch

Once the head pointer has been reset, the next step is to checkout the rebased branch. This can be done by running the following command:

```shell
git checkout <rebased_branch_name>
```

This command will switch the current branch to the rebased branch.

### Step 3: Reset the Rebased Branch

Once the rebased branch has been checked out, the next step is to reset the rebased branch. This can be done by running the following command:

```shell
git reset --hard <commit_hash>
```

This command will reset the rebased branch to the specified commit hash.

### Step 4: Push the Changes

The final step is to push the changes to the remote repository. This can be done by running the following command:

```shell
git push -f origin <rebased_branch_name>
```

This command will push the changes to the remote repository and overwrite any changes that were made during the rebase.
