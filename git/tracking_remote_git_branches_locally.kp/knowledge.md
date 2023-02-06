---
title: Keep a local copy of all remote git branches
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can track all remote git branches as local branches by using the `git branch -r` command.
---

**Contents**

[TOC]

## Solution 

### Cloning the Remote Repository 

The first step to tracking all remote branches as local branches is to clone the remote repository. This can be done using the command `git clone <remote-repo-url>`. This will create a local copy of the remote repository in the current working directory. 

### Checking Out a Remote Branch 

Once the repository has been cloned, the next step is to check out the remote branch. This can be done using the command `git checkout -b <branch-name> <remote-repo-url>/<branch-name>`. This will create a local branch that tracks the remote branch with the same name. 

### Tracking All Remote Branches 

To track all remote branches as local branches, the command `git branch -r` can be used. This command will list all remote branches and their associated URLs. 

### Pulling Remote Changes 

Finally, to pull remote changes to the local branches, the command `git pull <remote-repo-url> <branch-name>` can be used. This will pull any changes from the remote repository to the local branch.
