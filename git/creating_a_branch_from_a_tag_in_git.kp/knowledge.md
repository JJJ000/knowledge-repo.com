---
title: What is the process for creating a new branch from a tag?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To create a new branch from a tag in Git, use the command `git checkout -b <new-branch-name> <tag-name>`.
---

**Contents**

[TOC]

#1 Create a New Branch
1. Checkout the tag you want to create from: `git checkout <tag-name>`
2. Create a new branch from the tag: `git checkout -b <branch-name>`

#2 Push the New Branch to Remote
1. Push the new branch to the remote: `git push --set-upstream origin <branch-name>`

#3 Verify the New Branch
1. Verify the new branch was created: `git branch -a`
2. Verify the new branch is pushed to the remote: `git ls-remote --heads origin`
