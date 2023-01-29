---
title: Git diff indicates that the subproject has been modified
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git diff indicates that the subproject has changes that have not been committed to the repository.
---

**Contents**

[TOC]

### Overview

Git diff is a command-line utility used to compare two versions of a file or a directory. When used on a subproject, it can detect changes between the current version and the last committed version. If the subproject is dirty, the output of the command will indicate that the subproject contains changes that have not been committed.

### What Does "Dirty" Mean?

In the context of Git, the term "dirty" refers to any changes that have been made to a subproject but not yet committed. These changes may include new files, modified files, or deleted files.

### How to Check If a Subproject Is Dirty?

The git diff command can be used to check if a subproject is dirty. This command will compare the current version of a subproject with the last committed version and display the differences between the two. If the output of the command indicates that the subproject is dirty, it means that the subproject contains changes that have not yet been committed.

### How to Commit Changes?

Once changes to a subproject have been detected, they can be committed using the git commit command. This command will add the changes to the repository and make them part of the project's history.
