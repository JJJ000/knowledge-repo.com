---
title: What is the distinction between 'origin/master' and 'origin master' in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Origin/master refers to the remote branch, while origin master refers to a local branch that is tracking the remote branch.
---

**Contents**

[TOC]

#1 Origin/Master
Origin/master is a remote-tracking branch. This is a local copy of the remote master branch. This copy is automatically updated when the remote repository changes. It allows users to work with the remote repository without having to directly interact with it.

#2 Origin Master
Origin master is a local branch that is tracking the remote master branch. This branch is updated when changes are made to the remote master branch. This branch is not automatically updated when changes are made to the remote repository, and users must manually pull changes from the remote repository to update their local branch.
