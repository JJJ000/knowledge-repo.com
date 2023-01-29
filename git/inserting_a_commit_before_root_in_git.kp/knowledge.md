---
title: How can I add a commit prior to the initial commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: It is not possible to insert a commit before the root commit in Git.
---

**Contents**

[TOC]

### Introduction

Git is a distributed version control system that allows users to track the changes made to their projects over time. One of the key features of Git is its ability to track the history of a project, including the root commit. In some cases, it may be necessary to insert a commit before the root commit in order to make changes to the project’s history. In this article, we will discuss how to insert a commit before the root commit in Git.

### Steps to Insert a Commit Before the Root Commit

1. Check the root commit: Before you can insert a commit before the root commit, you need to identify the root commit. To do this, run the following command: `git log --oneline`. This will show you a list of all the commits in your repository, with the root commit at the top.

2. Check out the commit before the root commit: Once you have identified the root commit, you can check out the commit before it by running the following command: `git checkout <commit-id>`. This will check out the commit before the root commit so that you can make changes to it.

3. Make your changes: Once you have checked out the commit before the root commit, you can make the changes you want to make. This could include adding, modifying, or deleting files.

4. Commit your changes: Once you have made the changes you want to make, you can commit them by running the following command: `git commit -m “<message>”`. This will create a new commit with your changes and insert it before the root commit.

### Conclusion

In this article, we discussed how to insert a commit before the root commit in Git. We discussed the steps required to check out the commit before the root commit, make changes to it, and commit the changes. With these steps, you can easily insert a commit before the root commit in Git.
