---
title: Switch to a different branch when there are unsaved changes on the current one
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can either commit or stash the changes before checking out another branch, or use the `--force` flag to discard the changes.
---

**Contents**

[TOC]

### Stash Changes

The first step is to stash any changes on the current branch. This can be done by running the command `git stash`. This will store any changes on the current branch, allowing you to switch to another branch without committing them.

### Checkout New Branch

Once the changes have been stashed, you can checkout the new branch with the command `git checkout <branch-name>`. This will switch the current branch to the specified branch.

### Unstash Changes

Once you are on the new branch, you can unstash the changes from the previous branch with the command `git stash pop`. This will apply the stashed changes to the new branch.

### Commit Changes

Finally, if you want to commit the changes to the new branch, you can do so with the command `git commit -m "<commit message>"`. This will commit the changes to the new branch.
