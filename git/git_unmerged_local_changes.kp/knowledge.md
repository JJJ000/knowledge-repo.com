---
title: Git cannot revert local changes (error path ... has not been merged)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You need to either commit or reset the changes to undo them.
---

**Contents**

[TOC]

### Overview

Git is a popular version control system used to track changes to files and directories. When working with Git, it is possible to make local changes that cannot be undone. This is usually due to the fact that the path in question is unmerged. This article will explain what it means for a path to be unmerged and how to resolve this issue.

### What is Unmerged?

In Git, a file or directory is said to be unmerged when it has been modified in the local repository but not yet merged into the remote repository. This means that the changes made to the file or directory have not been shared with anyone else and are not part of the main branch of the project.

### How to Resolve

The most common way to resolve this issue is to first merge the changes into the remote repository. This can be done by using the git merge command. Once the changes have been merged into the remote repository, they can then be reverted back to their original state using the git reset command.

### Conclusion

In summary, unmerged paths can be a common issue when working with Git. To resolve this issue, the changes must first be merged into the remote repository and then reverted back to their original state. By following these steps, it is possible to undo local changes and keep the project in sync with the remote repository.
