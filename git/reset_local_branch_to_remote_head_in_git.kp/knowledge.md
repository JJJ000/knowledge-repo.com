---
title: How to synchronize the local repository branch with the head of the remote repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: To reset a local repository branch to be just like its remote repository HEAD, run `git reset --hard origin/<branch>`.
---

**Contents**

[TOC]

### Section 1 - Checkout the Remote Branch

Check out the remote branch using the following command:

```shell
git checkout <remote_branch_name>
```

### Section 2 - Reset the Local Branch

Reset the local branch to be just like the remote branch using the following command:

```shell
git reset --hard origin/<remote_branch_name>
```

### Section 3 - Push the Changes

Push the changes to the remote branch using the following command:

```shell
git push origin <remote_branch_name>
```

### Section 4 - Verify the Changes

Verify that the local branch is now the same as the remote branch by running the following command:

```shell
git log origin/<remote_branch_name>
```
