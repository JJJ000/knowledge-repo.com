---
title: Rearranging the words of the phrase, it could be rephrased as 'git's head and orig_head'
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: HEAD is a pointer to the current branch, while ORIG\_HEAD is a pointer to the previous branch.
---

**Contents**

[TOC]

### ORIG_HEAD

ORIG_HEAD is a pointer in the Git repository that stores the previous HEAD. This pointer is updated when a new commit is created.

### Use Cases

ORIG_HEAD can be used to undo a commit that has already been made. It can also be used to restore a repository to its original state prior to a commit being made.

### Benefits

The ORIG_HEAD pointer allows users to quickly and easily undo a commit without having to manually reset the repository. This can be especially useful when working with multiple branches and complex repositories.

### Limitations

ORIG_HEAD is only updated when a new commit is created. If a commit is undone using the ORIG_HEAD pointer, any changes made after the commit will be lost. Additionally, the ORIG_HEAD pointer is not updated if the repository is reset or a branch is switched.
