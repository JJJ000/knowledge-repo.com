---
title: What steps can I take to fix the "not something we can merge" error in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Resolve the conflict by manually editing the conflicting files and committing the changes.
---

**Contents**

[TOC]

### 1. Identify the Problem

When attempting to perform a merge, Git may throw an error stating "not something we can merge". This error indicates that Git is unable to automatically resolve the conflicts between the two branches.

### 2. Analyze the Conflict

In order to resolve the conflict, it is necessary to analyze the differences between the two branches and determine which changes should be kept and which should be discarded. This can be done by examining the differences between the two branches using a diff tool or by manually inspecting the changes.

### 3. Resolve the Conflict

Once the differences between the two branches have been identified, it is necessary to manually resolve the conflict by editing the files in question. This can be done by manually editing the files or by using a merge tool to interactively resolve the conflicts.

### 4. Commit the Changes

Once the conflicts have been resolved, the changes must be committed to the repository. This can be done by using the `git commit` command or by using a graphical user interface. After the changes have been committed, the merge can be completed and the conflict will be resolved.
