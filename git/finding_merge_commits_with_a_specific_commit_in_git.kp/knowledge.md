---
title: Identify the merge commit that incorporates a particular commit
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git log --merges --ancestry-path <commit>` to find the merge commit which includes a specific commit.
---

**Contents**

[TOC]

# Section 1 - Using git log

Using `git log` command, you can find the merge commit which include a specific commit.

1. To find the merge commit which include a specific commit, use the following command: 

`git log --merges --ancestry-path <commit-hash>`

2. Replace `<commit-hash>` with the hash of the commit you want to find the merge commit for.

# Section 2 - Using gitk

Using `gitk` command, you can also find the merge commit which include a specific commit.

1. To find the merge commit which include a specific commit, use the following command:

`gitk --merges --ancestry-path <commit-hash>`

2. Replace `<commit-hash>` with the hash of the commit you want to find the merge commit for.

# Section 3 - Using git show

Using `git show` command, you can also find the merge commit which include a specific commit.

1. To find the merge commit which include a specific commit, use the following command:

`git show --merges --ancestry-path <commit-hash>`

2. Replace `<commit-hash>` with the hash of the commit you want to find the merge commit for.

# Section 4 - Using git branch

Using `git branch` command, you can also find the merge commit which include a specific commit.

1. To find the merge commit which include a specific commit, use the following command:

`git branch --merges --ancestry-path <commit-hash>`

2. Replace `<commit-hash>` with the hash of the commit you want to find the merge commit for.
