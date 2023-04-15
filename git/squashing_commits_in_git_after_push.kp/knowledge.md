---
title: What is the process for combining multiple commits into one after they have been pushed to a remote repository in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To squash commits that have already been pushed, use the interactive rebase command with the `squash` option.
---

**Contents**

[TOC]

### Checkout Previous Commit

To squash commits that have been pushed to a remote repository, you must first checkout the commit before the ones you want to squash. This can be done with the following command:

`git checkout <commit-hash>`

### Rebase

Once you have checked out the previous commit, you can use the `git rebase` command to squash the commits together. The command to do this is as follows:

`git rebase -i HEAD~<number-of-commits>`

This command will open an editor, where you can change the `pick` commands to `squash` for the commits you want to squash together.

### Push Changes

Once you have finished squashing the commits, you must push the changes to the remote repository. This can be done with the following command:

`git push -f origin <branch-name>`

### Cleanup

Finally, you should run a `git gc` command to clean up any unnecessary files that may have been created during the rebase process. This can be done with the following command:

`git gc --prune=now`
