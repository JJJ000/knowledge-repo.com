---
title: Rejected push of master branch due to non-fast-forward condition
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: A non-fast-forward merge occurs when a commit has been made to the remote branch since the local branch was created, and Git refuses to overwrite the remote changes.
---

**Contents**

[TOC]

### Introduction

When working with Git, it is important to understand the concept of a non-fast-forward merge. This type of merge occurs when a branch is merged into a master branch, but the master branch contains commits that are not present in the branch being merged. In this case, Git will not allow the branch to be merged into the master branch without a manual intervention. 

### What is a non-fast-forward merge?

A non-fast-forward merge occurs when a branch is merged into a master branch, but the master branch contains commits that are not present in the branch being merged. This type of merge requires a manual intervention from the user in order to be successful. In this situation, Git will not automatically merge the branch into the master branch, and the user must manually resolve any conflicts that arise.

### How to resolve a non-fast-forward merge

When attempting to merge a branch into a master branch that contains commits that are not present in the branch being merged, the user must first manually resolve any conflicts that arise. This can be done by using the git merge command with the --no-ff option. This will allow the user to manually resolve any conflicts that arise before the branch is merged into the master branch.

### Conclusion

In conclusion, a non-fast-forward merge occurs when a branch is merged into a master branch, but the master branch contains commits that are not present in the branch being merged. This type of merge requires a manual intervention from the user in order to be successful, and the user must manually resolve any conflicts that arise before the branch is merged into the master branch.
