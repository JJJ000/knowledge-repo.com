---
title: What is preventing me from pushing to this bare repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You cannot push to a bare repository because it does not contain a working tree.
---

**Contents**

[TOC]

### Permissions

In order to push to a bare repository, the user must have the proper permissions to write to the repository. Generally, the user must have write access to the repository in order to be able to push to it. 

### Configuration

The user must also have the proper configuration settings in order to push to the repository. This includes making sure that the user's local repository is configured to push to the bare repository.

### Branching

The user must also make sure that the local repository is on the correct branch before attempting to push to the bare repository. If the user is trying to push to a branch that does not exist in the bare repository, the push will fail.

### Remote Tracking

Finally, the user must make sure that the local repository is tracking the remote repository before attempting to push. If the local repository is not tracking the remote repository, the push will fail.
