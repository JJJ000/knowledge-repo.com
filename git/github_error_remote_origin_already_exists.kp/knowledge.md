---
title: An error occurred there is already an existing remote repository named 'origin' on github
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The error `fatal remote origin already exists` means that the remote repository has already been added to the local repository.
---

**Contents**

[TOC]

### What is the Error?

The error "fatal: remote origin already exists" is an error message that appears when attempting to add a remote repository to a local repository in Git. 

### What Causes the Error?

This error occurs when a user attempts to add a remote repository to a local repository that already has a remote repository associated with it. This can occur if the user is attempting to add a new remote repository, or if the user has previously added a remote repository and is now attempting to add it again. 

### How to Resolve the Error

The error can be resolved by first removing the existing remote repository and then adding the new remote repository. This can be done using the following commands:

`git remote remove origin`

`git remote add origin [remote repository URL]`

### Conclusion

The error "fatal: remote origin already exists" is an error message that appears when attempting to add a remote repository to a local repository in Git. The error can be resolved by first removing the existing remote repository and then adding the new remote repository.
