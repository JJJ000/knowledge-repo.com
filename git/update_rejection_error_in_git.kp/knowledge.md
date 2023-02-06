---
title: The updates were not accepted because the remote version has changes that are not present in your local version
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: This error occurs when trying to push commits to a remote repository that contains commits that are not present in the local repository.
---

**Contents**

[TOC]

# Overview
This error occurs when the remote repository contains commits that you don't have locally. This can happen when someone else has pushed commits to the remote repository before you.

# Causes
The most common cause of this error is when someone else has pushed commits to the remote repository before you. It can also occur when you have deleted a branch that has commits that someone else has pushed. 

# Solutions
The best way to fix this error is to pull the latest commits from the remote repository. This will update your local repository with the commits that are on the remote. You can then push your own commits to the remote repository.

If you have deleted a branch that has commits that someone else has pushed, you can create a new branch and pull the latest commits from the remote repository. This will add the commits to the new branch.
