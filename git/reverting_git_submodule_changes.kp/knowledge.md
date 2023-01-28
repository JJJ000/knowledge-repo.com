---
title: What is the process for undoing my modifications to a git submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git submodule update --init --recursive` to revert changes to a git submodule.
---

**Contents**

[TOC]

### Revert Submodule to Previous Commit
1. Navigate to the submodule directory:
   `cd <path/to/submodule>`
2. Checkout the commit you want to revert to:
   `git checkout <commit_hash>`
3. Commit the changes:
   `git commit -m "Revert to <commit_hash>"`

### Update Parent Repository
1. Navigate to the parent repository:
   `cd <path/to/parent_repo>`
2. Add the changes to the index:
   `git add <path/to/submodule>`
3. Commit the changes:
   `git commit -m "Revert submodule to <commit_hash>"`
