---
title: What is the process for combining multiple git commits into a single commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To squash all git commits into one, use the `git rebase -i` command with the `squash` option.
---

**Contents**

[TOC]

#1 Create a new branch

First, create a new branch off of the branch you want to squash the commits into. This will be the branch in which you will squash the commits.

#2 Rebase the branch

Next, rebase the branch with the commits you want to squash. To do this, use the command: 

`git rebase -i HEAD~<number of commits>`

This will open up an interactive rebase window.

#3 Squash the commits

In the interactive rebase window, you will see a list of commits you want to squash. Change the word 'pick' to 'squash' on each commit you want to squash.

#4 Finalize the rebase

Finally, save the rebase window and complete the rebase. Your commits should now be squashed into one commit.
