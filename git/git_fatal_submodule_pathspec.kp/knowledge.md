---
title: Git fatal error pathspec is located inside a submodule
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Yes, a pathspec can be in a submodule.
---

**Contents**

[TOC]

## Introduction
Git is a version control system that allows developers to track changes in their code. When working with Git, it is possible to encounter a fatal error stating that the pathspec is in a submodule. This error occurs when a user attempts to checkout a submodule from a repository.

## What is a Pathspec?
A pathspec is a string that specifies the location of a file or directory within a repository. This can include the branch, file name, or directory name. When working with Git, a pathspec is used to identify which files or directories should be included in a given operation.

## What is a Submodule?
A submodule is a repository within a larger repository. This allows developers to include external code within their project without having to copy the entire repository. Submodules are useful for sharing code between different projects, as well as for keeping track of external dependencies.

## How to Resolve the Error
When attempting to checkout a submodule, the pathspec must be specified. To do this, the user must provide the full path to the submodule, including the branch and directory name. Once the correct pathspec is provided, the error should be resolved.
