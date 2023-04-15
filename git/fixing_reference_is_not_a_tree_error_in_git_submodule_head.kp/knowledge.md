---
title: The error 'git submodule head reference is not a tree' means that the reference being used is not a valid tree object
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The error occurs when the submodule reference points to an object that is not a commit or tree.
---

**Contents**

[TOC]

### What is a Git Submodule?
A Git submodule is a special type of repository that is nested inside another repository. It allows developers to keep track of external code inside their own repositories. This makes it easier to keep track of changes and dependencies in a project.

### What Causes the Error?
The 'reference is not a tree' error occurs when a Git submodule is not properly initialized or updated. This can happen if the submodule is not properly set up in the parent repository, or if the submodule has been moved or deleted.

### How to Fix the Error
The best way to fix the error is to make sure that the submodule is properly initialized and updated. This can be done by running the 'git submodule init' and 'git submodule update' commands in the parent repository.

### Conclusion
Git submodules can be a useful tool for managing external code, but it is important to make sure that they are properly initialized and updated. If the 'reference is not a tree' error occurs, running the 'git submodule init' and 'git submodule update' commands should be able to resolve the issue.
