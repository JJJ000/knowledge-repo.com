---
title: What is the best way to separate a git commit located in the past?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can use the `git rebase -i` command to interactively edit the commit history and split a commit into multiple commits.
---

**Contents**

[TOC]

1. **Find the Commit:**
   Use the `git log` command to find the commit in your repository's history.

2. **Create a New Branch:**
   Create a new branch from the commit you found in the previous step.

3. **Revert the Commit:**
   Use the `git revert` command to revert the commit you found in the previous step.

4. **Commit the Changes:**
   Commit the changes made by reverting the commit to your new branch.
