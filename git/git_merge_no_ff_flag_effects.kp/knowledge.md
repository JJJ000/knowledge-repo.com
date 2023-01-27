---
title: What is the result of using the "--no-ff" flag when running "git merge"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: The `--no-ff` flag prevents Git from performing a fast-forward merge, which creates a merge commit even when the branch could be fast-forwarded.
---

**Contents**

[TOC]

### What Does the Flag Do
The `--no-ff` flag stands for "no fast-forward" and prevents Git from performing a "fast-forward" merge when merging branches. A fast-forward merge is when Git moves the current branch pointer to the incoming branch, effectively combining the two branches without creating a merge commit.

### When to Use the Flag
The `--no-ff` flag should be used when you want to create a merge commit even when a fast-forward merge is possible. This is useful when you want to keep a record of when the branches were merged and create a distinct commit in the history.

### Benefits of Using the Flag
Using the `--no-ff` flag can help to keep the commit history of a project clean and organized. It can also make it easier to track down when a particular change was introduced into the codebase.

### Drawbacks of Using the Flag
The main drawback of using the `--no-ff` flag is that it can create a lot of unnecessary merge commits in the commit history, which can make it more difficult to navigate. Additionally, it can make it more difficult to identify which commits are related to a particular feature or bug fix.
