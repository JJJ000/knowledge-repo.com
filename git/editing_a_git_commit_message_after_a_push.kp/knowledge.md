---
title: Updating a git commit message after it has been pushed to the remote repository, as long as no one has pulled from the remote
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can`t change a git commit message after a push, as the commit is already part of the remote repository`s history.
---

**Contents**

[TOC]

### Reverting the Commit

1. Revert the commit using `git revert <commit-hash>`
2. Push the reverted commit to the remote repository

### Editing the Commit Message

1. Checkout the commit using `git checkout <commit-hash>`
2. Amend the commit message using `git commit --amend`
3. Push the amended commit to the remote repository
