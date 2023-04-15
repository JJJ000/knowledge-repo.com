---
title: What is the best way to revert a git repository to a particular commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can rollback a git repository to a specific commit by using the `git reset` command with the commit hash.
---

**Contents**

[TOC]

### Using git reset

1. Checkout the commit you want to rollback to: `git checkout <commit_hash>`
2. Reset the repository to the commit: `git reset --hard`

### Using git revert

1. Checkout the commit you want to rollback to: `git checkout <commit_hash>`
2. Revert the repository to the commit: `git revert <commit_hash>`
