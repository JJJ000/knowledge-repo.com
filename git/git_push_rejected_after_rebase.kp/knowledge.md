---
title: The push to the git repository was denied after the feature branch was rebased
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You must force-push the rebased branch to the remote repository in order for the changes to take effect.
---

**Contents**

[TOC]

### Rebase

Rebasing is a process of taking all the changes that have been made on one branch and applying them on top of another branch. This can be done to both feature branches and the main branch.

### Git Push Rejected

When a git push is rejected after a feature branch rebase, it means that the changes made on the feature branch are not compatible with the changes made on the main branch. This could be due to conflicts in the code, or due to changes made on the main branch that were not present on the feature branch.

### Resolving Conflicts

In order to resolve the conflict, you must first identify the source of the conflict. This can be done by looking at the changes made to both branches and determining which ones are in conflict. Once the source of the conflict is identified, you can then resolve the conflict by either manually merging the conflicting changes or by using a tool such as Git Merge Tool.

### Preventing Rejected Git Pushes

In order to prevent rejected git pushes after a feature branch rebase, it is important to regularly rebase the feature branch against the main branch. This will ensure that any changes made on the main branch are also present on the feature branch, thus avoiding any conflicts. Additionally, it is important to use a version control system such as Git to keep track of changes and ensure that all changes are properly merged.
