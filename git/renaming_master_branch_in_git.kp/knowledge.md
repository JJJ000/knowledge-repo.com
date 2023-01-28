---
title: Change the name of the master branch in both local and remote git repositories
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: To rename the local and remote master branch, use the command `git branch -m master <newname>` followed by `git push origin master` and `git push origin <newname>`.
---

**Contents**

[TOC]

### Local Repository
1. Check out the current branch: `git checkout master`
2. Create a new branch: `git branch new_master`
3. Switch to the new branch: `git checkout new_master`
4. Push the new branch to the remote repository: `git push origin new_master`

### Remote Repository
1. Rename the master branch on the remote repository: `git branch -m master new_master`
2. Push the changes to the remote repository: `git push origin :master`
3. Push the new branch to the remote repository: `git push origin new_master`
4. Set the new branch as the default branch: `git push --set-upstream origin new_master`
