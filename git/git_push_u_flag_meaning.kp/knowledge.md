---
title: What is the purpose of the -u flag when using the command 'git push -u origin master'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The -u flag stands for `upstream` and sets the branch specified by origin and master as the upstream branch for the current branch.
---

**Contents**

[TOC]

# Definition
The -u flag in git push -u origin master is a shorthand for setting up a local branch to track a remote branch.

# Usage
The -u flag is used to set up a local branch to track a remote branch. When used with git push, it will set the upstream branch for the local branch.

# Benefits
The -u flag helps to keep the local and remote branches in sync. It also simplifies the process of pushing changes to the remote repository.

# Syntax
The syntax for using the -u flag with git push is: git push -u <remote> <branch>.
