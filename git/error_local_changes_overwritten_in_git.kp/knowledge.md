---
title: Warning checking out this branch will replace the changes you have made to the following files
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Your local changes would be lost and overwritten by the checkout.
---

**Contents**

[TOC]

**Staged Files**

Staged files are files that have been added to the staging area. These files have been marked as ready to be committed and are tracked in the git repository. If a file is staged and you attempt to checkout a different branch, any local changes to the file will be overwritten.

**Unstaged Files**

Unstaged files are files that have not been added to the staging area. These files are not tracked in the git repository and any local changes to the file will not be overwritten when checking out a different branch.

**Ignored Files**

Ignored files are files that have been specified in the .gitignore file. These files are not tracked in the git repository and any local changes to the file will not be overwritten when checking out a different branch.

**Tracked Files**

Tracked files are files that have been added to the staging area and committed to the git repository. These files are tracked in the git repository and any local changes to the file will be overwritten when checking out a different branch.
