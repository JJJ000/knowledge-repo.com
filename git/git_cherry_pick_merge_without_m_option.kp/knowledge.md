---
title: Git cherry-pick states that "...38c74d is a merge, but the -m option was not specified."
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Cherry-pick cannot be used to merge commits, so the -m option must be specified.
---

**Contents**

[TOC]

### Overview

When using the `git cherry-pick` command, it is possible to receive an error message stating that a certain commit is a merge but no -m option was given. This error message is given when the user attempts to cherry-pick a commit that is a merge commit, but does not include the `-m` option in the command. 

### What is a Merge Commit?

A merge commit is a commit that combines two or more branches of a repository. When a merge commit is created, it has two or more parent commits, each of which represents the changes made in a different branch. 

### What is the -m Option?

The `-m` option is used when cherry-picking a merge commit. This option allows the user to specify which parent commit should be used when cherry-picking the merge commit. Without this option, git does not know which parent commit to use, resulting in the error message given. 

### How to Resolve the Error

To resolve the error, the user must specify the `-m` option when cherry-picking the merge commit. This option should be followed by the number of the parent commit that should be used. For example, if the user wanted to cherry-pick the first parent commit, they would use the command `git cherry-pick -m 1 <commit-hash>`.
