---
title: How to move a branch to the latest commit in the repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To fast-forward a branch to head in Git, use the command `git merge --ff-only <branch>`.
---

**Contents**

[TOC]

### Step 1: Fetch the Latest Updates

In order to fast-forward a branch to head in Git, the first step is to fetch the latest updates from the remote repository. This can be done by running the following command:

`git fetch`

### Step 2: Checkout the Branch

The next step is to checkout the branch that you want to fast-forward. This can be done by running the following command:

`git checkout <branch_name>`

### Step 3: Merge the Latest Updates

Once the branch has been checked out, the next step is to merge the latest updates from the remote repository into the branch. This can be done by running the following command:

`git merge origin/<branch_name>`

### Step 4: Push the Changes

Finally, the changes need to be pushed to the remote repository. This can be done by running the following command:

`git push origin <branch_name>`
