---
title: Retrieve from the source with removed remote branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To fetch from origin with deleted remote branches, use the `--prune` flag.
---

**Contents**

[TOC]

### Fetching Deleted Branches

### Step 1: Check Local Branches

Before attempting to fetch deleted branches from the remote, it is important to check if the deleted branch still exists in the local repository. This can be done by running the command `git branch -a` to list all of the local branches. If the deleted branch is still present in the list, it can be easily recovered.

### Step 2: Fetch Remote Branches

If the deleted branch is not present in the local repository, it can be fetched from the remote by running the command `git fetch origin`. This will fetch all of the branches from the remote repository and make them available locally.

### Step 3: Check Remote Branches

Once the remote branches have been fetched, they can be viewed by running the command `git branch -r`. This will list all of the remote branches, including the deleted branch.

### Step 4: Checkout Deleted Branch

The deleted branch can then be checked out by running the command `git checkout <branch_name>`. This will switch the current working branch to the deleted branch. Any changes made to the branch can then be committed and pushed back to the remote.
