---
title: How can I commit a file in one branch while ignoring it in another branch using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a .gitignore file in the branch you want to ignore the file in, and commit the file in the other branch.
---

**Contents**

[TOC]

## Step 1: Create a .gitignore File

Create a file in the root of your repository called `.gitignore` and add the name of the file you would like to ignore.

## Step 2: Commit the .gitignore File

Commit the `.gitignore` file to the branch where you would like to ignore the file.

## Step 3: Checkout the Other Branch

Checkout the branch where you would like to have the file committed.

## Step 4: Add and Commit the File

Add and commit the file to the branch.
