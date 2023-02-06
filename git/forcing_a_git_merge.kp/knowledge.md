---
title: Forcefully merging with git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git merge with force overwrite can be done using the `--force` option.
---

**Contents**

[TOC]

# Force Merge

A force merge is a type of merge that allows you to overwrite existing changes in a branch with changes from another branch. This can be useful when you want to discard changes from a branch and replace them with changes from another branch.

## When to Use Force Merge

Force merge should be used when you need to discard changes from a branch and replace them with changes from another branch. This could be done if, for example, the changes in the branch have caused an issue that cannot be resolved.

## How to Force Merge

To force merge changes from one branch into another, you must first switch to the branch you wish to merge into. Then, use the `git merge --force` command, followed by the name of the branch you wish to merge from.

## Potential Issues

When force merging, it is important to be aware that any changes that were made in the branch you are merging from will be discarded. This could cause issues if the changes were important. Therefore, it is important to understand the changes that you are merging before using the `git merge --force` command.
