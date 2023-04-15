---
title: How do head, working tree, and index differ in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The HEAD is a pointer to the current branch and commit, the working tree is the files that are being tracked, and the index is a staging area for changes to be committed.
---

**Contents**

[TOC]

### HEAD
HEAD is a pointer to the last commit in the current branch. It points to the commit that will be checked out when a user runs `git checkout` without specifying a branch or commit.

### Working Tree
The working tree is the directory containing the files that are being tracked by Git. It is the directory that a user sees when they run `git status` or `git log`.

### Index
The index is a staging area between the working tree and the repository. It is used to store changes that will be committed to the repository. Changes are staged in the index before they are committed to the repository.
