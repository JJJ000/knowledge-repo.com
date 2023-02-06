---
title: Remove the local git branches after they have been removed from the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, run `git fetch --prune` to delete local branches that have been deleted on the remote repo.
---

**Contents**

[TOC]

# Section 1: Delete Locally

To delete a local branch, use the `git branch -d` command followed by the branch name. For example, if the branch name is `my-branch`, the command would look like `git branch -d my-branch`.

# Section 2: Verify Deletion

Once the branch is deleted locally, you can verify its deletion by running the command `git branch` which will list all the branches in your local repo. The branch that was just deleted should not appear in the list.

# Section 3: Prune Remote Branches

To delete the remote branch, use the command `git fetch --prune` which will delete all the remote branches that have been deleted from the remote repo.

# Section 4: Verify Deletion

Once the remote branch is deleted, you can verify its deletion by running the command `git branch -r` which will list all the remote branches. The branch that was just deleted should not appear in the list.
