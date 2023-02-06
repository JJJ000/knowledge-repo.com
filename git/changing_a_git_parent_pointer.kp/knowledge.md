---
title: Changing the git parent reference to a different one
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can set a different parent pointer by using the `git branch --set-upstream-to` command.
---

**Contents**

[TOC]

**1. Understanding Git Parent Pointers**

Git parent pointers are the references that link a commit to its parent commit. Each commit in a repository has one parent commit, except for the initial commit which has no parent. When a new commit is created, the parent pointer is set to the commit that preceded it in the repository.

**2. Changing the Parent Pointer**

To change the parent pointer of a commit, the user must use the `git rebase` command. This command allows the user to move a commit to a different location in the repository, and in doing so, change the commit's parent pointer.

**3. Using the Rebase Command**

To use the `git rebase` command, the user must first identify the commit they want to move. The user then needs to specify the new parent commit for the commit they want to move. Finally, the user must execute the `git rebase` command, which will move the commit to the specified new parent.

**4. Potential Issues**

When changing a commit's parent pointer, the user should be aware that it is a potentially dangerous operation. If the parent pointer is changed incorrectly, it can cause conflicts and issues in the repository. Therefore, it is important to make sure the parent pointer is set correctly before executing the `git rebase` command.
