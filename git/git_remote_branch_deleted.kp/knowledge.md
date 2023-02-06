---
title: View a list of local and remote branches, including those that have been deleted from the remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, it is possible for `git branch -av` to show a remote branch that no longer exists.
---

**Contents**

[TOC]

# Overview

When a user runs the command `git branch -av`, it will show all local branches, as well as all remote branches. This includes remote branches that have been deleted. 

# Why Does This Occur?

Git stores information about remote branches in its local repository. When a user runs `git branch -av`, it will show all branches, even if they have been deleted from the remote repository. 

# How To Remove A Remote Branch

In order to remove a remote branch, the user must first delete it from the remote repository. This can be done with the command `git push <remote> --delete <branch>` where `<remote>` is the name of the remote repository and `<branch>` is the name of the branch to be deleted. 

# How To Remove A Remote Branch From Local Repository

Once the remote branch is deleted, the user must then delete the local copy of the branch. This can be done with the command `git branch -d <branch>` where `<branch>` is the name of the branch to be deleted. This will remove the local copy of the branch, and the branch will no longer show up when running `git branch -av`.
