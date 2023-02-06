---
title: Change the name of a git submodule
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To rename a git submodule, use the `git mv` command.
---

**Contents**

[TOC]

## Step 1: Change the Path of the Submodule

To rename a git submodule, the first step is to change the path of the submodule. This can be done by editing the `.gitmodules` file and changing the `url` and `path` of the submodule.

## Step 2: Change the Name of the Submodule Folder

The second step is to change the name of the submodule folder. This can be done by navigating to the submodule folder and renaming it.

## Step 3: Update the Index

The third step is to update the index. This can be done by running the command `git add -u` to update the index with the changes made.

## Step 4: Commit the Changes

The fourth and final step is to commit the changes. This can be done by running the command `git commit -m "Renamed submodule"`.
