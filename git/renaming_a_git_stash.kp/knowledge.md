---
title: What is the procedure for changing the name of a git stash?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You cannot rename a git stash.
---

**Contents**

[TOC]

### Option 1:
1. Create a new branch from the stash: `git stash branch <branch-name>`
2. Delete the original stash: `git stash drop`

### Option 2:
1. Create a new commit from the stash: `git stash show -p | git commit -F -`
2. Rename the commit: `git commit --amend --no-edit --reset-author`
3. Delete the original stash: `git stash drop`
