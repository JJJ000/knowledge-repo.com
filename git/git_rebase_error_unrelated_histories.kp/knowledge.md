---
title: Git will not combine unrelated histories when performing a rebase
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Git will refuse to merge unrelated histories on rebase, and the `--allow-unrelated-histories` flag must be used to override this.
---

**Contents**

[TOC]

### What is Unrelated Histories? 
Unrelated histories occurs when two branches have diverged so much that their commits do not share a common ancestor. This means that Git cannot accurately determine which changes should be kept and which should be discarded. This can occur when two branches are created from different points in the repository's history, or when one branch is rebased onto another branch.

### Why Does Git Refuse to Merge Unrelated Histories?
Git refuses to merge unrelated histories because it cannot accurately determine which changes should be kept and which should be discarded. When two branches have diverged so much that their commits do not share a common ancestor, it is impossible for Git to accurately determine which changes should be kept and which should be discarded. This can lead to conflicts that cannot be resolved automatically and require manual intervention.

### How to Resolve Unrelated Histories
The best way to resolve unrelated histories is to use a rebase. A rebase is a process in which the commits from one branch are applied onto another branch. This allows Git to accurately determine which changes should be kept and which should be discarded.

### Alternatives to Rebasing
If a rebase is not possible, then the two branches must be manually merged. This involves manually resolving any conflicts that arise and carefully checking the resulting merge commit to ensure that all changes are correct. This is a time-consuming process and should be avoided if possible.
