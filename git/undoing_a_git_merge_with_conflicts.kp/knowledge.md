---
title: How to reverse a git merge with conflicting changes
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To undo a git merge with conflicts, use `git merge --abort`.
---

**Contents**

[TOC]

### 1. Checkout the Commit Before the Merge

To undo a git merge with conflicts, the first step is to check out the commit before the merge. This can be done by using the `git log` command to view the commit history, then using the `git checkout` command to check out the commit before the merge.

### 2. Reset the Branch

Once the commit before the merge has been checked out, the next step is to reset the branch to the commit before the merge. This can be done by using the `git reset` command with the `--hard` flag.

### 3. Push the Changes

The final step is to push the changes to the remote repository. This can be done by using the `git push` command with the `--force` flag.

### 4. Clean Up Local Working Copy

Once the changes have been pushed to the remote repository, the final step is to clean up the local working copy. This can be done by using the `git clean` command with the `-d` flag. This will delete any unversioned files that were created during the merge.
