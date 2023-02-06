---
title: Error 'master' is not a valid object name
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The string `master` is not a valid commit SHA-1 hash, and therefore cannot be used as an object name in Git.
---

**Contents**

[TOC]

## What is a Valid Object Name in Git?
A valid object name in Git is a reference to a specific commit. A valid object name must follow a specific pattern and is usually a combination of letters, numbers, and/or symbols.

## What is 'master' in Git?
In Git, 'master' is the default branch name. It is the main branch where all the changes are committed and pushed to.

## Why is 'master' Not a Valid Object Name?
Since 'master' is a branch name and not a commit reference, it is not a valid object name in Git. A valid object name must point to a specific commit and not a branch.

## What is the Alternative to 'master'?
The alternative to 'master' is to use the commit reference (SHA-1 hash) of the commit that you want to refer to. This commit reference can be found in the output of the `git log` command.
