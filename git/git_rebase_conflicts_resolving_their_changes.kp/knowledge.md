---
title: What steps should be taken to incorporate "their" changes during a git rebase that is experiencing conflicts?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Resolve the conflicts by selecting which changes to keep and then continue the rebase.
---

**Contents**

[TOC]

### Identify Conflicting Commits

Before attempting to resolve any conflicts, it is important to identify which commits are in conflict. This can be done by running the `git status` command, which will provide a list of files that have been modified and need to be resolved.

### Resolve Conflicts

Once the conflicting commits have been identified, the next step is to resolve the conflicts. This can be done by manually editing the conflicting files and resolving the conflicts within them. Alternatively, a tool like `git mergetool` can be used to help with the process.

### Add Resolved Files

Once the conflicts have been resolved, the next step is to add the resolved files back into the repository. This can be done by running the `git add` command, followed by the list of files that have been modified.

### Continue Rebase

Once the conflicts have been resolved and the files have been added, the next step is to continue the rebase process. This can be done by running the `git rebase --continue` command, which will continue the rebase process and incorporate the changes from the conflicting commits.
