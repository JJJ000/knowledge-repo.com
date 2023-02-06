---
title: What is the equivalent of svn externals in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git does not have an exact equivalent to SVN externals, but submodules can be used to achieve a similar effect.
---

**Contents**

[TOC]

# Submodules

Git has a feature called submodules which is similar to SVN externals. Submodules allow you to link a repository inside another repository. This allows you to keep your repositories organized and to keep track of the changes made in each repository.

# Cloning

Another way to achieve a similar effect to SVN externals is to clone the external repository into your main repository. This allows you to have the same files and folders in both repositories. However, it does not allow you to keep track of the changes made in the external repository.

# Subtrees

Subtrees are a variation of submodules, but they allow you to keep track of the changes made in the external repository. This is done by merging the external repository into your main repository. This allows you to keep track of the changes made in the external repository, but it does not allow you to keep the repositories organized.

# Git Subtree

Git subtree is a tool that allows you to manage multiple repositories as a single repository. It allows you to keep track of the changes made in each repository, while also keeping them organized. It is similar to SVN externals in that it allows you to keep track of the changes made in each repository.
