---
title: Error when attempting to push to git refusing to make changes to a branch that has already been checked out
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git will not allow you to push to a branch that is currently checked out.
---

**Contents**

[TOC]

**1. Overview**

Git Push error: refusing to update checked out branch is a common error message when attempting to push changes to a remote Git repository. This error occurs when a user attempts to push changes to a branch that is already checked out on a local machine. This error is caused by Git's safety feature that prevents changes from being pushed to a branch that is currently checked out on a local machine.

**2. Causes**

The main cause of this error is when a user attempts to push changes to a branch that is already checked out on their local machine. This is because Git's safety feature prevents changes from being pushed to a branch that is currently checked out on a local machine.

**3. Solutions**

The best way to solve this error is to first switch to another branch on the local machine. Once the user has switched to another branch, they can then push their changes to the remote repository. Another solution is to use the `git push --force` command, which will override the safety feature and allow the user to push changes to the checked out branch. 

**4. Conclusion**

Git Push error: refusing to update checked out branch is a common error message when attempting to push changes to a remote Git repository. This error is caused by Git's safety feature that prevents changes from being pushed to a branch that is currently checked out on a local machine. The best way to solve this error is to first switch to another branch on the local machine or use the `git push --force` command.
