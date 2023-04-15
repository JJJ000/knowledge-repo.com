---
title: What is the best way to store only the staged changes in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the command `git stash --keep-index` to stash only staged changes in Git.
---

**Contents**

[TOC]

### Staging Changes

In order to stash only staged changes in Git, the first step is to stage the desired changes. This can be done with the following command:

`git add <filename>`

This command will stage the changes made to the specified file.

### Stashing Changes

After the desired changes have been staged, they can be stashed with the following command:

`git stash --keep-index`

This command will stash only the staged changes and leave the unstaged changes intact.

### Verifying Stash

To verify that only the staged changes were stashed, the following command can be used:

`git stash show -p`

This command will show the changes that were stashed and will allow you to verify that only the changes that were staged were stashed.

### Unstashing Changes

Once the changes have been stashed, they can be unstashed with the following command:

`git stash pop`

This command will restore the stashed changes and remove them from the stash.
