---
title: Move the subdirectory into its own separate git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Create a new Git repository in the subdirectory and push the contents of the subdirectory to the new repository.
---

**Contents**

[TOC]

### Preparation

Before detaching the subdirectory into a separate Git repository, it is important to consider the following steps:

1. Make sure all changes in the subdirectory have been committed to the original repository.
2. Create a new, empty repository for the detached subdirectory.
3. Identify the commit in the original repository which will be used as the starting point for the new repository.

### Detaching

Once the preparation steps have been taken, the subdirectory can be detached into a separate Git repository using the following steps:

1. Create a new branch in the original repository with the name of the new repository.
2. Checkout the new branch.
3. Copy the subdirectory to the new branch.
4. Add and commit the subdirectory to the new branch.
5. Push the new branch to the new repository.

### Cleanup

Once the subdirectory has been successfully detached into a separate repository, the following steps should be taken to clean up the original repository:

1. Delete the new branch from the original repository.
2. Remove the subdirectory from the original repository.
3. Commit and push the changes to the original repository.
