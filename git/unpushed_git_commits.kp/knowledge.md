---
title: Show commits made in git that have not been pushed to the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git commits not pushed to the origin yet are stored locally in the local repository.
---

**Contents**

[TOC]

### Local Commits
Local commits are commits that have been made to your local repository but not yet pushed to the remote. To view local commits, run the command `git log --branches --not --remotes`

### Unpushed Commits
Unpushed commits are commits that have been made to your local repository and have been pushed to the remote, but have not yet been merged into the origin. To view unpushed commits, run the command `git log origin..HEAD`

### Uncommitted Changes
Uncommitted changes are changes that have been made to your local repository but have not yet been committed. To view uncommitted changes, run the command `git diff`

### Unstaged Changes
Unstaged changes are changes that have been made to your local repository but have not yet been staged for commit. To view unstaged changes, run the command `git diff --cached`
