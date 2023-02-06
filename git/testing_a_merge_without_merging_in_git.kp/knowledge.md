---
title: How to preview a merge before committing it?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the `git merge --no-commit --no-ff` command to test a merge without actually merging first in Git.
---

**Contents**

[TOC]

# 1. Using git diff

Using `git diff` you can compare two branches or commits without merging. This will allow you to see the changes between two branches, and determine if the merge will be successful.

# 2. Using git merge --no-commit

Using `git merge --no-commit` will allow you to merge two branches without actually committing the changes. This will allow you to test the merge and determine if it will be successful before actually committing.

# 3. Using git merge --no-ff

Using `git merge --no-ff` will allow you to merge two branches without fast-forwarding the changes. This will allow you to test the merge and determine if it will be successful before actually committing.

# 4. Using git revert

Using `git revert` you can revert a merge without actually merging. This will allow you to test the merge and determine if it will be successful before actually committing.
