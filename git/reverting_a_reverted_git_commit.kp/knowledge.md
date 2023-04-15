---
title: How can I undo a reverted git commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the `git revert` command with the SHA-1 hash of the reverted commit to create a new commit that undoes the changes of the reverted commit.
---

**Contents**

[TOC]

### Step 1: Find the Commit Hash

The first step to un-revert a git commit is to find the commit hash of the reverted commit. You can use the `git log` command to view the commit history and find the commit hash.

### Step 2: Checkout the Commit

Once you have the commit hash, you can use the `git checkout` command to checkout the commit. This will create a new branch with the commit hash as its name.

### Step 3: Merge the Branch

Now that you have the commit checked out, you can use the `git merge` command to merge the commit into the main branch. This will restore the reverted commit.

### Step 4: Push the Commit

Finally, you can use the `git push` command to push the commit to the remote repository. This will make the un-reverted commit available to other users.
