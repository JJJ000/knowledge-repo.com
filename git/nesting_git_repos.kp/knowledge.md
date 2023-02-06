---
title: Keep a git repository within another git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, this is possible by using `git submodules`.
---

**Contents**

[TOC]

# Yes, It Is Possible

Git allows you to maintain a repository inside another repository. This is commonly referred to as "nesting" repositories.

## How To Nest Repositories

Nesting repositories is relatively straightforward. To do so, simply create a folder in the parent repository and then use the `git init` command to create a new repository inside the folder.

## Benefits of Nesting Repositories

Nesting repositories can be useful if you need to keep multiple related projects together in the same repository. For example, you might want to keep a project and its associated documentation in the same repository.

## Caveats

Nesting repositories can make it more difficult to manage and keep track of changes. It can also be difficult to keep the nested repositories in sync with the parent repository, as any changes made to the parent repository will not be reflected in the nested repositories.
