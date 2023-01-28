---
title: What steps should I take to correct a mistake in committing to the wrong git branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Revert the commit, checkout the correct branch, and commit the changes again.
---

**Contents**

[TOC]

### 1. Check Out the Correct Branch

The first step to fix committing to the wrong Git branch is to check out the correct branch. This can be done by using the `git checkout` command followed by the name of the branch you wish to switch to.

### 2. Revert the Wrong Commit

Once you have checked out the correct branch, you can then use the `git revert` command to revert the wrong commit. This command will undo any changes made in the wrong commit and reset the branch to its previous state.

### 3. Re-Commit the Changes

After reverting the wrong commit, you can re-commit the changes to the correct branch by using the `git commit` command. This will ensure that the changes are applied to the correct branch.

### 4. Push the Changes

Finally, you can push the changes to the correct branch by using the `git push` command. This will ensure that the changes are applied to the remote repository and can be accessed by other users.
