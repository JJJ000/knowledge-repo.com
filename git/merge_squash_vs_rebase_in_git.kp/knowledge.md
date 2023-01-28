---
title: What are the distinctions between using merge --squash and rebase?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Merge --squash combines multiple commits into one commit, while rebase rewrites the commit history by creating new commits for each commit in the original branch.
---

**Contents**

[TOC]

### Merge --Squash
Merge --squash is a command used to combine multiple commits into a single commit. It is used to make a complex history of commits look like a single commit. This can be useful when you want to clean up the commit history of a feature branch before merging it into the main branch.

### Rebase
Rebase is a command used to move a branch onto a different commit. It is used to rewrite the commit history of a branch, usually to make it look cleaner. Rebase can also be used to move a branch onto a different branch, such as a feature branch onto the main branch. This is useful when you want to keep the feature branch separate from the main branch, but still want to keep the feature branch up to date.
