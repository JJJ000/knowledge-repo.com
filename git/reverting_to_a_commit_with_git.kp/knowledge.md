---
title: How do I use git to go back to a particular commit using its commit id?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To revert to a specific commit based on commit id with Git, use the command `git reset --hard <commit\_id>`.
---

**Contents**

[TOC]

### Step 1: Find the Commit ID

The first step to reverting to a specific commit is to find the commit ID. The commit ID is a unique identifier that is associated with each commit. It can be found in the output of the `git log` command.

### Step 2: Revert to the Commit

Once the commit ID has been found, the next step is to run the `git revert <commit_id>` command. This command will revert the repository to the state it was in at the time of the specified commit.

### Step 3: Push the Changes

Once the repository has been reverted to the desired commit, the changes need to be pushed to the remote repository. This can be done with the `git push` command.

### Step 4: Verify the Changes

The final step is to verify that the changes have been successfully pushed to the remote repository. This can be done by running the `git log` command and verifying that the commit ID that was reverted to is present in the output.
