---
title: How to transfer changes from the incorrect branch to an existing topic branch in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Checkout the existing topic branch, then use `git cherry-pick` to copy the changes from the wrong branch.
---

**Contents**

[TOC]

### 1. Checkout the Correct Branch

To copy changes to an existing topic branch, first ensure that you are on the correct branch. To do this, use the `git checkout` command, followed by the name of the branch you want to switch to.

For example, if you want to switch to the `my-topic-branch` branch, you would use the command:

```git
git checkout my-topic-branch
```

### 2. Stash Changes

Once you are on the correct branch, you will need to stash any changes that you have made on the wrong branch. To do this, use the `git stash` command. This will save any changes you have made and allow you to switch branches without losing your changes.

### 3. Copy Changes

Once you are on the correct branch and have stashed any changes, you can copy the changes from the wrong branch using the `git cherry-pick` command. This command allows you to select specific commits from one branch and apply them to another branch.

For example, if you want to copy the last commit from the `wrong-branch` to the `my-topic-branch` branch, you would use the command:

```git
git cherry-pick wrong-branch~1
```

### 4. Unstash Changes

Finally, once you have copied the changes to the correct branch, you can unstash the changes you made on the wrong branch. To do this, use the `git stash pop` command. This will apply the stashed changes to the current branch.
