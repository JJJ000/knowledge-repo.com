---
title: What is the best way to get rid of .ds_store files in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run the command `git rm --cached $(git ls-files -i -X .gitignore -o --exclude-standard)` to remove all .DS\_Store files from a Git repository.
---

**Contents**

[TOC]

### Solution 1
1. Use the `.gitignore` file
   - Create a `.gitignore` file in the root of your repository
   - Add the line `.DS_Store` to the `.gitignore` file
   - Commit the `.gitignore` file
   - All new `.DS_Store` files will now be ignored

### Solution 2
1. Remove existing `.DS_Store` files
   - Use the command `find . -name '.DS_Store' -type f -delete` to delete all existing `.DS_Store` files
   - Commit the changes

### Solution 3
1. Use a Git hook
   - Create a `pre-commit` hook in the `.git/hooks` directory
   - Add the command `find . -name '.DS_Store' -type f -delete` to the `pre-commit` hook
   - All `.DS_Store` files will now be deleted before every commit
