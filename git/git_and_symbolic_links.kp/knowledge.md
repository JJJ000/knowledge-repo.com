---
title: What is git's approach to symbolic links?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git stores symbolic links as normal files with their target path as the content.
---

**Contents**

[TOC]

### Symbolic Link Creation

When a symbolic link is created, Git will record it as a file in the repository. This means that when the repository is cloned, the symbolic link will also be cloned.

### Symbolic Link Updates

Git will track changes to symbolic links, just like any other file in the repository. This means that when a symbolic link is updated, it will be recorded in the repository just like any other file.

### Symbolic Link Deletion

If a symbolic link is deleted, Git will record the deletion in the repository. This means that when the repository is cloned, the symbolic link will not be present.

### Symbolic Link Conflicts

If two different branches contain changes to the same symbolic link, Git will not be able to automatically merge the changes. In this case, a manual merge will be required to resolve the conflict.
