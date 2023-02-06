---
title: What is the process for making git push automatically set the upstream without using the -u flag?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git push --set-upstream` command to automatically set upstream without the -u flag.
---

**Contents**

[TOC]

## Configuring Default Push

1. Open the command line and navigate to the local repository.

2. Type the command `git config --global push.default upstream` to set the default push behavior.

## Setting Upstream

1. Type the command `git remote add origin <remote repository URL>` to add the remote repository URL as the origin.

2. Type the command `git push -u origin master` to set the upstream branch for the local repository.

## Testing Push

1. Make changes to the local repository and commit them.

2. Type the command `git push` to push the changes to the remote repository.

3. Verify that the changes were successfully pushed to the remote repository.
