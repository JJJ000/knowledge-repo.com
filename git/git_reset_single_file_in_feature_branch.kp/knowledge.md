---
title: Revert a single file in the feature branch to its state in the master branch using git reset
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git checkout master -- <file>; git checkout <branch> -- <file>` to reset the file in the feature branch to be the same as in master.
---

**Contents**

[TOC]

### Checkout File from Master
1. Checkout the file from master: 
`git checkout master -- <file_name>`

### Merge File from Master
2. Merge the file from master: 
`git merge master -- <file_name>`

### Push Changes to Feature Branch
3. Push the changes to the feature branch: 
`git push origin <feature_branch>`

### Reset File
4. Reset the file to be the same as in master: 
`git reset HEAD <file_name>`
