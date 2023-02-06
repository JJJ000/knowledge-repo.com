---
title: After performing a rebase, there will be multiple copies of the same git commits in the same branch
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, git commits can be duplicated in the same branch after doing a rebase.
---

**Contents**

[TOC]

## Rebase
Rebase is a command that is used to integrate changes from one branch into another. It works by taking all the commits from one branch and applying them onto another branch. This process can cause some commits to be duplicated in the same branch if the commits in the source branch already exist in the target branch. 

## Causes
The most common cause of duplicate commits is when a rebase is done from a branch that has commits that already exist in the target branch. This can happen when the source branch is ahead of the target branch and contains commits that were already merged into the target branch.

## Prevention
The best way to prevent duplicate commits is to ensure that the source and target branches are up-to-date before performing the rebase. This can be done by performing a git pull on both branches to ensure that all the commits from the source branch have been merged into the target branch.

## Resolution
If duplicate commits have already been created, they can be removed by using the git rebase --interactive command. This command allows the user to select which commits they want to keep and which ones they want to discard. Once the desired commits have been selected, the rebase can be completed and the duplicate commits will be removed.
