---
title: Troubleshooting git merges
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git merge errors occur when the same file has been modified in two different branches and Git is unable to automatically merge the changes.
---

**Contents**

[TOC]

### Merge Conflicts
Merge conflicts occur when two branches have different changes to the same file. This can happen when someone has made changes to a file on one branch, and someone else has made changes to the same file on a different branch. Git will not be able to automatically merge these changes, and will instead prompt the user to manually resolve the conflict.

### Resolving Merge Conflicts
When a merge conflict occurs, the user will need to manually review the changes that were made on both branches and decide which changes to keep and which changes to discard. This can be done using a text editor or a graphical merge tool.

### Common Causes of Merge Conflicts
Merge conflicts are often caused by changes to the same lines of code or changes to overlapping sections of a file. They can also be caused by changes to the same files on different branches.

### Preventing Merge Conflicts
Merge conflicts can be prevented by ensuring that all changes to a file are made on the same branch. It is also important to ensure that all branches are kept up to date with the latest changes from the main branch. Finally, it is important to communicate changes that are being made to a file so that multiple people are not making changes to the same file at the same time.
