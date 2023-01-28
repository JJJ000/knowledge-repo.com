---
title: Reworking git conflicts
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git conflict markers are special symbols used to indicate where a conflict has occurred during a merge.
---

**Contents**

[TOC]

### What are Git Conflict Markers?
Git conflict markers are special lines of text that are automatically inserted into files when a merge conflict occurs. These markers help identify the conflicting sections so they can be resolved.

### How Do Git Conflict Markers Work?
Git conflict markers are inserted into a file when a merge conflict occurs. They indicate the conflicting sections and provide information about the changes made by each branch. The markers can be used to identify the conflicting sections and resolve the conflict.

### What Do Git Conflict Markers Look Like?
Git conflict markers appear as special lines of text in the file. They begin with a “<<<<<<<” and end with a “>>>>>>>”. In between these markers are the conflicting sections of code.

### How to Resolve Git Conflict Markers
Git conflict markers can be resolved by manually editing the conflicting sections. The conflicting sections should be reviewed and the changes made by each branch should be reviewed. Once the changes have been reviewed, the conflicting sections should be merged and the conflict markers should be removed.
