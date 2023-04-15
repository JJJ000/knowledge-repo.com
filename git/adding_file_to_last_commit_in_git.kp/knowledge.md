---
title: What is the process for attaching a file to the most recent commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the command `git commit --amend` to add a file to the last commit.
---

**Contents**

[TOC]

#1 Using Amend

1. Run `git commit --amend`
2. This will open an editor where you can make changes to the commit message
3. Add the file to the staging area using `git add <filename>`
4. Commit the changes with the new message

#2 Using Reset

1. Run `git reset --soft HEAD^`
2. Add the file to the staging area using `git add <filename>`
3. Commit the changes using `git commit -m "<message>"`
