---
title: There was an error when attempting to pull from the remote repository the remote reference is different from the expected reference
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: A pull error is likely caused by a mismatch between the local and remote repository versions.
---

**Contents**

[TOC]

### Problem
When running `git pull`, the following error is encountered:

`error: remote ref is at but expected`

### Causes
This error can occur due to a few different reasons. 

1. The remote repository has been updated and the local repository has not been updated to reflect the changes. 
2. The local repository has been updated with a branch that does not exist in the remote repository. 
3. The local repository has been updated with a tag that does not exist in the remote repository. 

### Solutions
1. To resolve the issue, first try running `git fetch` to update the local repository with the changes from the remote repository.
2. If the local repository has been updated with a branch or tag that does not exist in the remote repository, delete the branch or tag locally and then try running `git pull` again.
3. If the issue persists, try running `git reset --hard` to reset the local repository to the state of the remote repository.
