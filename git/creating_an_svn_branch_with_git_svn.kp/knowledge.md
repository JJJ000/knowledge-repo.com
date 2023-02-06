---
title: How can I create a new subversion branch using git-svn?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git svn branch <new-branch-name>` to create a new SVN branch via Git.
---

**Contents**

[TOC]

# Creating a New SVN Branch via Git

## Prerequisites
Before creating a new SVN branch via Git, you must ensure that your local Git repository is set up to track the remote SVN repository. This can be done by running the command `git svn init` followed by the URL of the remote SVN repository.

## Creating the Branch
Once the local Git repository is set up to track the remote SVN repository, you can create a new SVN branch via Git by running the command `git svn branch <branch_name>`. This will create a new branch in the remote SVN repository and push it to the local Git repository.

## Pushing the Branch
To push the new SVN branch to the remote SVN repository, you can run the command `git svn dcommit`. This will push the changes to the remote SVN repository and create a new branch in the remote SVN repository.

## Verifying the Branch
To verify that the new SVN branch has been created, you can run the command `git branch -a` to list all the branches in the remote SVN repository. The newly created branch should be listed in the output.
