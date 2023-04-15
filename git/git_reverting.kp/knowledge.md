---
title: Revert a git repository to a specific commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To revert back to a certain commit, use the `git revert` command followed by the commit hash.
---

**Contents**

[TOC]

### Step 1: Find the Commit

In order to revert back to a certain commit, you must first find the commit. This can be done by running the `git log` command. This command will list out all the commits in the repository.

### Step 2: Revert to the Commit

Once you have identified the commit, you can revert back to it using the `git revert` command. This command will create a new commit that reverts the changes made in the specified commit.

### Step 3: Push the Revert

Once the revert has been created, you can push it to the remote repository using the `git push` command. This will update the remote repository with the reverted commit.

### Step 4: Clean Up

Finally, you can clean up any other commits that were created after the reverted commit using the `git reset` command. This will reset the branch to the reverted commit, allowing you to start from a clean slate.
