---
title: What is the process for completely replacing a local branch with a remote branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To replace a local branch with a remote branch entirely, use the command `git fetch <remote\_name> <branch\_name> && git reset --hard <remote\_name>/<branch\_name>`.
---

**Contents**

[TOC]

### Step 1: Delete the Local Branch

You can delete the local branch by running the following command:

`git branch -d <branch_name>`

This will delete the local branch and all its commits.

### Step 2: Fetch the Remote Branch

Next, you need to fetch the remote branch from the remote repository. You can do this by running the following command:

`git fetch origin <remote_branch_name>`

This will fetch the remote branch and all its commits to your local repository.

### Step 3: Checkout the Remote Branch

Now, you need to checkout the remote branch. You can do this by running the following command:

`git checkout <remote_branch_name>`

This will switch your local branch to the remote branch.

### Step 4: Push the Remote Branch

Finally, you need to push the remote branch to the remote repository. You can do this by running the following command:

`git push origin <remote_branch_name>`

This will push the remote branch to the remote repository and replace the local branch with the remote branch.
