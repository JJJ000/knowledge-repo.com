---
title: How to remove local tracking branches that are no longer present on the remote?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git fetch --prune` to prune local tracking branches that do not exist on remote anymore.
---

**Contents**

[TOC]

1. Identifying Local Tracking Branches That Do Not Exist on Remote
----------------------------------------------------

To identify the local tracking branches that no longer exist on the remote, you can use the command `git branch -vv`. This command will list all the local branches and their corresponding remote tracking branches. If a branch is listed with an asterisk (*) next to it, then it means that the branch does not exist on the remote.

2. Pruning Local Tracking Branches
---------------------------------

Once you have identified the local tracking branches that do not exist on the remote, you can prune them using the command `git branch -d <branch_name>`. This will delete the local tracking branch. Note that this command will only delete the branch if it has been fully merged into the current branch.

3. Updating Remote Tracking Branches
------------------------------------

You can update the remote tracking branches with the command `git fetch --prune`. This command will update the remote tracking branches and delete any branches that have been deleted on the remote.

4. Verifying the Pruning
------------------------

To verify that the local tracking branches have been successfully pruned, you can use the command `git branch -vv` again. This command will list all the local branches and their corresponding remote tracking branches. If a branch is listed with an asterisk (*) next to it, then it means that the branch does not exist on the remote.
