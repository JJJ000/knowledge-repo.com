---
title: Revert to an earlier commit and commit the changes as a new commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Checkout the old commit and then use `git commit --amend` to make it a new commit.
---

**Contents**

[TOC]

# Step 1: Checkout the Desired Commit

In order to checkout a desired commit, the following command can be used:

`git checkout <commit-hash>`

Where `<commit-hash>` is the hash of the desired commit.

# Step 2: Make Changes

Once the desired commit has been checked out, changes can be made to the code. Once the changes have been made, they can be added to the staging area using the command:

`git add <file-name>`

Where `<file-name>` is the name of the file that has been changed.

# Step 3: Commit Changes

Once the changes have been added to the staging area, they can be committed using the command:

`git commit -m "<message>"`

Where `<message>` is the commit message describing the changes that have been made.

# Step 4: Push Changes

Finally, the changes can be pushed to the remote repository using the command:

`git push origin <branch-name>`

Where `<branch-name>` is the name of the branch that the changes should be pushed to.
