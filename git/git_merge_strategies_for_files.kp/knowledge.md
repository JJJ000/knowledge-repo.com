---
title: Select a git merging approach for particular files ("ours", "mine", "theirs")
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The best merge strategy for specific files depends on the context and the desired outcome.
---

**Contents**

[TOC]

### Ours

The "ours" strategy is the most conservative of the merge strategies. It takes the version of the file from the branch that is doing the merging and discards all changes from the other branch. This strategy is useful in cases where the branch being merged into is the main branch and the changes from the other branch are not desired.

### Mine

The "mine" strategy is the opposite of the "ours" strategy. It takes the version of the file from the branch that is being merged and discards all changes from the branch doing the merging. This strategy is useful in cases where the branch being merged into is a feature branch and the changes from the other branch are not desired.

### Theirs

The "theirs" strategy is the most aggressive of the merge strategies. It takes the version of the file from the branch that is being merged and discards all changes from the branch doing the merging. This strategy is useful in cases where the changes from the other branch are desired and the branch being merged into is the main branch.

### Manual

The "manual" strategy is the most flexible of the merge strategies. It allows the user to manually select which changes from each branch should be included in the merged file. This strategy is useful in cases where the changes from both branches are desired and the user wants to manually select which changes should be included in the merged file.
