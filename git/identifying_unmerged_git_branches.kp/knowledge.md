---
title: What are the unmerged git branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git branch --no-merged` to find unmerged Git branches.
---

**Contents**

[TOC]

1. Identify Unmerged Branches 
   - Using `git branch --no-merged`
   - This command will list all the branches that have not yet been merged into the current branch.

2. Identify Unmerged Commits 
   - Using `git log --no-merges`
   - This command will list all the commits that have not yet been merged into the current branch.

3. Identify Unmerged Changes 
   - Using `git diff --name-only`
   - This command will list all the changes that have not yet been merged into the current branch.

4. Identify Unmerged Files 
   - Using `git ls-files --others --exclude-standard`
   - This command will list all the files that have not yet been merged into the current branch.
