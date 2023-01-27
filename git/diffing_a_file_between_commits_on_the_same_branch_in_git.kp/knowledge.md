---
title: What is the difference between two commits of the same file on the same branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git diff <commit1> <commit2> <file>` to diff the same file between two different commits on the same branch in Git.
---

**Contents**

[TOC]

### Using `git diff`
1. Check out the commit you want to compare the file against:
   ```
   git checkout <commit-hash>
   ```
2. Retrieve the file from the commit:
   ```
   git show <commit-hash>:<file-name> > <file-name>
   ```
3. Check out the other commit you want to compare the file against:
   ```
   git checkout <other-commit-hash>
   ```
4. Retrieve the file from the other commit:
   ```
   git show <other-commit-hash>:<file-name> > <other-file-name>
   ```
5. Use `git diff` to compare the two files:
   ```
   git diff <file-name> <other-file-name>
   ```

### Using `git log`
1. Check out the commit you want to compare the file against:
   ```
   git checkout <commit-hash>
   ```
2. Use `git log` to get the commit hash of the other commit you want to compare the file against:
   ```
   git log --oneline -- <file-name>
   ```
3. Check out the other commit:
   ```
   git checkout <other-commit-hash>
   ```
4. Use `git diff` to compare the two files:
   ```
   git diff <commit-hash>:<file-name> <other-commit-hash>:<file-name>
   ```
