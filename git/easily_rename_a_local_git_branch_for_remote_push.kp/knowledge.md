---
title: What is the simplest way to rename a local git branch and push it to a remote repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use the command `git push <remote> <local-branch><remote-branch>` to push a local Git branch to a remote with a different name.
---

**Contents**

[TOC]

## Step 1: Create a New Branch

1. Create a new branch on your local machine using `git checkout -b <new_branch_name>`

## Step 2: Push the Local Branch to the Remote

1. Push the local branch to the remote with `git push -u origin <new_branch_name>`

## Step 3: Create the New Remote Branch

1. Create the new remote branch with `git push origin <new_branch_name>:<new_remote_branch_name>`

## Step 4: Set the Remote Branch as the Default

1. Set the new remote branch as the default with `git branch --set-upstream-to=origin/<new_remote_branch_name>`
