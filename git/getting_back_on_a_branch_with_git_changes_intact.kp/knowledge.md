---
title: Is there a simple way to return to a branch and maintain my changes while using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, you can use the `git checkout` command with the `-b` option to create a new branch and switch to it while preserving the changes.
---

**Contents**

[TOC]

## Checkout the Branch

Git allows you to checkout a branch while keeping your changes. To do this, you can use the `git checkout` command. This command will switch you to the branch you specify while keeping any changes you have made.

## Stash Your Changes

If you do not want to switch branches with your changes, you can use the `git stash` command. This command will store your changes in a temporary place, allowing you to switch branches without committing them.

## Reapply Stashed Changes

After you have switched branches, you can reapply your stashed changes. To do this, you can use the `git stash apply` command. This command will apply your stashed changes to the current branch.

## Commit Your Changes

Finally, if you want to keep your changes, you can commit them to the branch. To do this, you can use the `git commit` command. This command will commit your changes to the current branch.
