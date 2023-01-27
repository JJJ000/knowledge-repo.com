---
title: How can I combine a particular commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To merge a specific commit in Git, use the `git cherry-pick <commit-hash>` command.
---

**Contents**

[TOC]

1. **Checkout the desired branch**
   - Checkout the branch you want to merge the commit into.

2. **Find the commit you want to merge**
   - Use `git log` to find the commit you want to merge.

3. **Merge the commit**
   - Use `git merge <commit-hash>` to merge the commit into the current branch.

4. **Push the changes**
   - Push the changes to the remote repository by using `git push`.
