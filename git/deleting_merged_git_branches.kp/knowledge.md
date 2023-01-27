---
title: What is the process for removing all git branches that have been merged?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Run `git branch --merged | grep -v `\*` | xargs -n 1 git branch -d` to delete all merged branches.
---

**Contents**

[TOC]

1. **Check Merged Branches:**
   Run the following command to view all merged branches:
   ```
   git branch --merged
   ```

2. **Delete Merged Branches:**
   Run the following command to delete all merged branches:
   ```
   git branch -d $(git branch --merged)
   ```

3. **Check Unmerged Branches:**
   Run the following command to view all unmerged branches:
   ```
   git branch --no-merged
   ```

4. **Delete Unmerged Branches:**
   Run the following command to delete all unmerged branches:
   ```
   git branch -D $(git branch --no-merged)
   ```
