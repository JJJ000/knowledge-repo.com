---
title: Is it possible to perform a partial revert in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can do a partial revert in Git by using the `git revert` command with the `--no-commit` option.
---

**Contents**

[TOC]

Yes, you can do a partial revert in GIT.

## Steps to Perform a Partial Revert 
1. Check out the commit you want to partially revert.
2. Use the `git reset` command to reset the index and working tree to the desired commit.
3. Use the `git checkout` command to check out the desired files from the desired commit.
4. Use the `git commit` command to commit the changes.
