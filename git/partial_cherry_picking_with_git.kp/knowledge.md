---
title: Selecting certain parts of a commit using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git can partially cherry-pick a commit by using the `--cherry-pick` option along with the commit hash.
---

**Contents**

[TOC]

### Choosing the Commit

To cherry-pick a commit, you must first identify the commit you want to pick. This can be done by viewing the commit log and finding the SHA-1 hash of the commit you want to pick.

### Cherry-Picking the Commit

Once you have identified the commit you want to pick, you can use the `git cherry-pick` command to pick the commit. This command takes the SHA-1 hash of the commit you want to pick as an argument. For example, the command `git cherry-pick <sha-1 hash>` can be used to pick a specific commit.

### Verifying the Commit

Once you have picked the commit, you should verify that the commit was picked correctly. This can be done by checking the commit log and verifying that the commit is present.

### Pushing the Commit

Once the commit has been verified, you can push the commit to the remote repository with the `git push` command. This will make the commit available to other users.
