---
title: What is the process for permanently deleting multiple commits from a remote branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git revert <commit-hash>` for each commit to be removed, then push the changes to the remote branch.
---

**Contents**

[TOC]

### Create a New Branch

1. Create a new branch from the commit you want to keep: 
`git branch new_branch <commit-id>`

### Rebase the Branch

2. Rebase the branch to remove the commits you don't want: 
`git rebase --onto new_branch <commit-id> <commit-id>`

### Push the New Branch

3. Push the new branch to the remote repository: 
`git push <remote-name> new_branch`

### Delete the Old Branch

4. Delete the old branch: 
`git push <remote-name> :old_branch`
