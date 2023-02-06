---
title: What merge strategy should I use when performing a git rebase?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can select a merge strategy for a git rebase by specifying the desired strategy with the `-s` option.
---

**Contents**

[TOC]

## Using the Interactive Rebase

The most common way to select a merge strategy for a git rebase is to use the interactive rebase feature. This is done by running `git rebase -i <commit>`, where `<commit>` is the commit to be rebased. This will open an editor window with a list of commits to be rebased. By default, all commits will be marked as `pick`. To change the merge strategy for a commit, simply change the `pick` to the desired strategy.

## Available Merge Strategies

The available merge strategies for a git rebase are `pick`, `reword`, `edit`, `squash`, `fixup`, and `exec`.

* `pick`: This is the default merge strategy. It will simply apply the commit as is.
* `reword`: This will apply the commit, but allow you to edit the commit message.
* `edit`: This will apply the commit, but allow you to edit the changes before they are applied.
* `squash`: This will combine the commit with the previous commit, allowing you to edit the commit message.
* `fixup`: This will combine the commit with the previous commit, but will discard the commit message.
* `exec`: This will allow you to run a shell command after the commit is applied.
