---
title: What command should be used with git and the command line to retain the local or remote file when merging?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the `git merge --strategy-option theirs` command to keep the local or remote file during a merge.
---

**Contents**

[TOC]

## Step 1: Check Out the Branch 

To keep the local file or the remote file during a merge using Git and the command line, the first step is to check out the branch that contains the changes you want to keep. If the changes are in the remote branch, you will need to check out the remote branch. This can be done with the following command: 

`git checkout -b <branch-name> <remote-name>/<branch-name>` 

If the changes are in the local branch, you can use the following command to check out the local branch: 

`git checkout <branch-name>`

## Step 2: Merge the Branches 

Once the branch that contains the changes you want to keep has been checked out, you can then merge the branches using the following command: 

`git merge <branch-name-to-merge-from>` 

This will merge the changes from the branch you checked out in Step 1 with the branch you are currently on. 

## Step 3: Resolve Conflicts 

During the merge process, you may encounter conflicts. To resolve conflicts, you will need to manually edit the conflicting files to choose which changes you want to keep. Once you have resolved the conflicts, you can add the files with the following command: 

`git add <file-name>` 

## Step 4: Commit the Changes 

Once you have resolved the conflicts, you can commit the changes with the following command: 

`git commit -m "Merge branch <branch-name>"` 

This will commit the changes to the repository and allow you to keep the local or remote file during the merge.
