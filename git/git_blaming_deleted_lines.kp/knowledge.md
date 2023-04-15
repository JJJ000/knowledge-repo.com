---
title: What is the best way to find out who last modified a deleted line using "git blame"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: It is not possible to `git blame` a deleted line.
---

**Contents**

[TOC]

### Method 1

1. Navigate to the commit that deleted the line in question. 
2. Copy the commit hash. 
3. Run the command `git blame <commit-hash> -- <file>`

### Method 2

1. Navigate to the commit that deleted the line in question. 
2. Copy the commit hash. 
3. Run the command `git log <commit-hash> -- <file>`
4. Find the line in question and note the commit hash associated with it.
5. Run the command `git blame <commit-hash> -- <file>`
