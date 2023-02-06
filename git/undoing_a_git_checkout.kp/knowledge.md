---
title: What is the process for reverting a checkout in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To undo a checkout in git, use the `git checkout` command with the commit hash or branch name that you want to switch back to.
---

**Contents**

[TOC]

## 1. Undo a Checkout Using Git Reset

1. Check the status of your repository: `git status`
2. If the repository is in a "detached HEAD" state, use the command `git reset --hard HEAD` to undo the checkout.
3. If the repository is not in a "detached HEAD" state, use the command `git reset --hard <commit-hash>` to undo the checkout.

## 2. Undo a Checkout Using Git Revert

1. Check the status of your repository: `git status`
2. Use the command `git revert <commit-hash>` to undo the checkout.

## 3. Undo a Checkout Using Git Checkout

1. Check the status of your repository: `git status`
2. Use the command `git checkout <commit-hash>` to undo the checkout.

## 4. Undo a Checkout Using Git Clean

1. Check the status of your repository: `git status`
2. Use the command `git clean -f` to undo the checkout.
