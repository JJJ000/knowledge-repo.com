---
title: Revert a specific commit that has been pushed to a remote git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To undo a particular commit that has been pushed to remote repos, use the command `git revert <commit-hash>`.
---

**Contents**

[TOC]

### Step 1: Revert the Commit

To undo a particular commit that has been pushed to the remote repository, you need to use the `git revert` command. This command creates a new commit that reverts the changes from the specified commit.

### Step 2: Push the Reverted Commit

Once you have reverted the commit, you need to push the reverted commit to the remote repository. To do this, you can use the `git push` command. Make sure to use the `--force` flag to ensure that your changes are pushed to the remote repository.

### Step 3: Remove the Reverted Commit

If you want to completely remove the reverted commit from the remote repository, you can use the `git push` command with the `--delete` flag. This will delete the commit from the remote repository.

### Step 4: Clean Up the Local Repository

Finally, you need to clean up your local repository by using the `git reset` command. This command will reset your local repository to the state it was in before you reverted the commit.
