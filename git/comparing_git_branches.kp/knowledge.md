---
title: What are the distinctions between two branches?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `git diff` command to view the differences between two branches in Git.
---

**Contents**

[TOC]

1. Using `git diff` 
   - `git diff <branch1> <branch2>`
   - This will show you the differences between two branches

2. Using `git log` 
   - `git log <branch1>..<branch2>`
   - This will show you a list of all the commits that are in one branch but not the other

3. Using `git show` 
   - `git show <commit>`
   - This will show you the changes associated with a particular commit

4. Using a Graphical Tool 
   - Most graphical git clients provide a visual representation of the differences between two branches.
