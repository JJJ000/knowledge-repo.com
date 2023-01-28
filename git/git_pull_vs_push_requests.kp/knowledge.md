---
title: Why isn't a 'git pull request' referred to as a 'push request'?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: A pull request is not called a push request because it is the process of requesting changes from a remote repository, rather than pushing changes to it.
---

**Contents**

[TOC]

### Reason 1: Push and Pull Have Different Meanings

In Git, the terms "push" and "pull" refer to two distinct operations. A "push" is used to update a remote repository with changes made to a local repository, while a "pull" is used to update a local repository with changes made to a remote repository.

### Reason 2: Push and Pull Requests Are Not the Same

A "push request" is a request to push a set of changes from a local repository to a remote repository. A "pull request" is a request to pull a set of changes from a remote repository to a local repository.

### Reason 3: Pull Requests Are More Common

In practice, pull requests are more common than push requests. This is because developers typically make changes to their local repositories and then submit those changes to a remote repository for review.

### Reason 4: Pull Requests Are Easier to Review

Pull requests are also easier to review than push requests. This is because pull requests allow developers to review changes before they are pushed to a remote repository, while push requests require developers to review changes after they have been pushed.
