---
title: What is the process for selecting specific commits from a remote branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To cherry-pick from a remote branch in Git, use the command `git cherry-pick <commit-hash>`.
---

**Contents**

[TOC]

# Step 1: Fetch the remote branch

Before cherry-picking from a remote branch in Git, you must first fetch the branch from the remote repository. This can be done with the following command:

`git fetch origin <remote-branch-name>`

# Step 2: Checkout the remote branch

Once the remote branch has been fetched, you must then checkout the branch in order to access the commits:

`git checkout -b <local-branch-name> origin/<remote-branch-name>`

# Step 3: Cherry-pick the commit

Once the remote branch has been checked out, you can then cherry-pick the desired commit with the following command:

`git cherry-pick <commit-hash>`

# Step 4: Push the changes

Once the cherry-pick is complete, you must then push the changes to the remote repository:

`git push origin <local-branch-name>`
