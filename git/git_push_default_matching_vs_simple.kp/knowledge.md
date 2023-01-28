---
title: What is the distinction between push.default "matching" and "simple" in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: `Matching` will push all local branches that have a remote branch with the same name, while `simple` will only push the current branch to the same name on the remote.
---

**Contents**

[TOC]

### Push.default "Matching"
This option sets the behavior of `git push` so that it will push all branches with the same name as the local branch to the remote repository. This is the default option since Git 2.0.

### Push.default "Simple"
This option sets the behavior of `git push` so that it will only push the current branch to the remote repository. This option is more conservative, as it will only push the current branch and not any other branches.

### Advantages of Push.default "Matching"
- Allows for pushing multiple branches at once
- Makes it easier to keep the remote repository in sync with the local repository

### Advantages of Push.default "Simple"
- More conservative approach, as it will only push the current branch
- Less chance of accidentally pushing unwanted branches or changes to the remote repository
