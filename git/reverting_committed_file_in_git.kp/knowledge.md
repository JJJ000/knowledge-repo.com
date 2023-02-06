---
title: Revert a committed file in git after pushing it
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, it is not possible to remove a committed file after it has been pushed to a remote repository.
---

**Contents**

[TOC]

## Option 1: Git Revert 

The simplest way to remove a file from a repository after it has been pushed is to use the `git revert` command. This command will create a new commit that undoes the changes made in the specified commit. 

To use `git revert`, you will need to know the commit hash for the commit that added the file. You can find this hash by running the `git log` command. Once you have the commit hash, you can run the command `git revert <commit-hash>` to undo the changes made in the specified commit.

## Option 2: Git Reset

Another way to remove a file from a repository after it has been pushed is to use the `git reset` command. This command allows you to reset the repository back to a previous commit. 

To use `git reset`, you will need to know the commit hash for the commit that you want to reset the repository back to. You can find this hash by running the `git log` command. Once you have the commit hash, you can run the command `git reset --hard <commit-hash>` to reset the repository back to the specified commit.

## Option 3: Git Filter-Branch

A third way to remove a file from a repository after it has been pushed is to use the `git filter-branch` command. This command allows you to rewrite the history of the repository by applying a custom filter. 

To use `git filter-branch`, you will need to know the name of the file that you want to remove. You can then run the command `git filter-branch --tree-filter 'rm -f <file-name>'` to remove the specified file from the repository.

## Option 4: Git Clean

The final way to remove a file from a repository after it has been pushed is to use the `git clean` command. This command allows you to remove untracked files from the working tree. 

To use `git clean`, you will need to know the name of the file that you want to remove. You can then run the command `git clean -f <file-name>` to remove the specified file from the repository.
