---
title: Questions about git workflows and the difference between rebasing and merging
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Git workflow is a set of processes for managing changes to a project, while rebase is a command to re-apply commits on top of another base tip, while merge is a command to combine multiple sequences of commits into one.
---

**Contents**

[TOC]

####Git Workflow
Git workflow is a set of guidelines that define how developers interact with a codebase. It includes how to create and merge branches, how to handle conflicts, and how to keep track of changes. Git workflow helps keep code organized and ensures that all changes are tracked and documented.

####Rebase vs. Merge
Rebasing and merging are two different approaches for managing changes in a codebase. Rebasing is the process of taking a branch and rewriting its history to apply changes from one branch to another. Merging is the process of combining two branches by taking the changes from one branch and applying them to another. 

Rebasing is often used when working on a feature branch, as it allows developers to keep their branch up to date with the main branch while still keeping a clean history. Merging is often used when two branches have diverged and need to be combined. Merging is also used when a feature branch is ready to be merged into the main branch.
