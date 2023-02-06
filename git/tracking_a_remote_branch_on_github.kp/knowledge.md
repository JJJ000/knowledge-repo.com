---
title: Monitor a newly established remote branch on github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To track a new remote branch created on GitHub, use the command `git checkout -b <branch-name> origin/<branch-name>`.
---

**Contents**

[TOC]

# Tracking a New Remote Branch

## Step 1: Clone the Repository

The first step in tracking a new remote branch is to clone the repository that contains the branch. This can be done using the `git clone` command. 

## Step 2: Check Remote Branches

After cloning the repository, the next step is to check the remote branches that are available. This can be done using the `git branch -r` command. This will list all the remote branches available in the repository.

## Step 3: Check Out the Remote Branch

Once the remote branch is identified, the next step is to check out the remote branch. This can be done using the `git checkout` command.

## Step 4: Track the Remote Branch

Finally, to track the remote branch, the `git branch --track` command can be used. This will create a local branch that tracks the remote branch.
