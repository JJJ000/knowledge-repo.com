---
title: How to undo a checkout of unstaged files and discard local changes in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git reset --hard` to discard local changes and undo the checkout.
---

**Contents**

[TOC]

### Step 1 - Reset the branch

In order to undo the checkout of unstaged files and discard local changes, you need to reset the branch to the last commit. To do this, use the `git reset` command with the `--hard` flag:

`git reset --hard`

This will reset the branch to the last commit and discard any local changes.

### Step 2 - Discard Unstaged Files

Next, you need to discard any unstaged files that were checked out. To do this, use the `git clean` command with the `-f` flag:

`git clean -f`

This will discard any unstaged files that were checked out.

### Step 3 - Push the Changes

Finally, you need to push the changes to the remote repository. To do this, use the `git push` command with the `--force` flag:

`git push --force`

This will push the changes to the remote repository and overwrite any existing commits.

### Step 4 - Verify the Changes

Once the changes have been pushed to the remote repository, you should verify that the changes were successful. To do this, use the `git log` command to view the commit history:

`git log`

This will show the commit history and verify that the changes were successful.
