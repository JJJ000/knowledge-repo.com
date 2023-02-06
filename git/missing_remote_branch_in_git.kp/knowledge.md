---
title: "the remote branches are not appearing when I run 'git branch -r'"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git fetch --all` to update the list of remote branches.
---

**Contents**

[TOC]

## Check Remote

First, it is important to check that the remote branch actually exists. To do this, run the command `git remote show origin` to list all branches on the remote repository. If the branch is not listed, it does not exist and cannot be tracked.

## Set Up Tracking

If the branch does exist, it may not be set up to be tracked locally. To do this, run the command `git branch --set-upstream-to origin/[branch-name]` to set up tracking for the specified branch.

## Fetch Remote

Once tracking is set up, the remote branch can be fetched and shown in the local repository. To do this, run the command `git fetch` to retrieve the latest version of the remote branch.

## View Remote

Finally, the remote branch can be viewed by running the command `git branch -r` to list all remote branches. The specified branch should now be visible in the list.
