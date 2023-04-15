---
title: Reverting a 'git push'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To undo a `git push`, you can use the command `git revert`.
---

**Contents**

[TOC]

### Step 1: Reset the Local Repository

To undo a `git push`, the first step is to reset the local repository to the state it was in before the push. This can be done by running the following command:

```git
git reset --hard HEAD~1
```

This will reset the local repository to the commit just before the push.

### Step 2: Reset the Remote Repository

The second step is to reset the remote repository to the same commit as the local repository. This can be done by running the following command:

```git
git push -f origin HEAD
```

This will reset the remote repository to the same commit as the local repository.

### Step 3: Push Local Changes

The third step is to push the local changes to the remote repository. This can be done by running the following command:

```git
git push origin <branch-name>
```

This will push the local changes to the remote repository.

### Step 4: Clean Up

The fourth and final step is to clean up any temporary files or changes that were made during the process. This can be done by running the following command:

```git
git clean -fd
```

This will delete any untracked files or directories that were created during the process.
