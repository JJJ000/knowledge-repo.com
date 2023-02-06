---
title: Undo a series of commits in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To revert a range of commits in git, use the `git revert` command with the range of commits you want to revert as arguments.
---

**Contents**

[TOC]

# Revert a Range of Commits

## Step 1: Identify the Range of Commits

Before reverting a range of commits, it is important to identify the range of commits to be reverted. This can be done by running the `git log` command to view the commit history. Each commit will have a unique identifier associated with it, such as a hash code. The range of commits to be reverted can then be identified by noting the hash codes of the start and end commits.

## Step 2: Revert the Range of Commits

Once the range of commits to be reverted has been identified, the `git revert` command can be used to revert the commits. This command takes the hash codes of the start and end commits as arguments. For example, the following command can be used to revert a range of commits between two commits with hash codes `abc123` and `def456`:

```
git revert abc123..def456
```

## Step 3: Push the Reverted Commits

After the range of commits has been reverted, the changes need to be pushed to the remote repository. This can be done using the `git push` command.

## Step 4: Clean Up the Reverted Commits

After the reverted commits have been pushed to the remote repository, any local copies of the commits should be removed. This can be done using the `git clean` command.
