---
title: Revert a file to a previous version using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the git reset command with a specific commit hash to rollback a file to an earlier version in Git.
---

**Contents**

[TOC]

# Step 1: Checkout the Desired Commit

To rollback a file to an earlier version using git, the first step is to check out the desired commit. To do this, use the following command:

`git checkout <commit_hash> <file_name>`

Where `<commit_hash>` is the SHA hash of the desired commit and `<file_name>` is the name of the file you want to rollback.

# Step 2: Create a New Branch

Once the desired commit is checked out, the next step is to create a new branch. This is done using the following command:

`git checkout -b <branch_name>`

Where `<branch_name>` is the name of the new branch.

# Step 3: Push the New Branch

Once the new branch is created, the next step is to push it to the remote repository. This is done using the following command:

`git push -u origin <branch_name>`

Where `<branch_name>` is the name of the new branch.

# Step 4: Merge the New Branch

Finally, the new branch needs to be merged into the master branch. This is done using the following command:

`git merge <branch_name>`

Where `<branch_name>` is the name of the new branch.
