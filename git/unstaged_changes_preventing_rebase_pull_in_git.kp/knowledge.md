---
title: Error cannot perform pull with rebase uncommitted changes present
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You must commit or stash your changes before you can pull with rebase.
---

**Contents**

[TOC]

# Stash Unstaged Changes

One way to handle unstaged changes in Git is to stash them. Stashing is a way to temporarily store changes that are not yet ready to be committed. To stash the changes, use the command `git stash`. This will store the changes in a special area called the "stash" and leave the working directory clean.

# Discard Unstaged Changes

Another way to handle unstaged changes in Git is to discard them. This can be done with the command `git checkout -- <file>`. This command will discard any changes that have been made to the specified file and revert it to the version in the most recent commit.

# Commit Unstaged Changes

If the changes are ready to be committed, they can be committed directly. To do this, use the command `git commit -a`. This will commit all changes that have been made, including those that are unstaged.

# Reset Unstaged Changes

Finally, it is possible to reset the changes back to the version in the most recent commit with the command `git reset --hard`. This command will discard any changes that have been made and reset the working directory to the version in the most recent commit.
