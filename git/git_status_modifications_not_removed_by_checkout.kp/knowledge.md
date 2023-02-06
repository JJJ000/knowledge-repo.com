---
title: Git status displays any changes that have been made, while git checkout -- <file> does not undo them
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git checkout -- <file> will reset the file to its last committed state, but will not remove the modifications.
---

**Contents**

[TOC]

# Overview

Git status can be used to check for changes made to files in a repository. Git checkout is a command used to switch branches or restore files to a previous version. While git status can show modifications, git checkout will not remove them.

# Git Status

Git status is a command used to check for changes made to files in a repository. It will show which files have been modified, added, or deleted. It can also show which branch the repository is currently on.

# Git Checkout

Git checkout is a command used to switch branches or restore files to a previous version. It can be used to switch between branches, undo changes to files, and restore deleted files. However, it will not remove modifications that have been made to files.

# Conclusion

In conclusion, git status can be used to check for changes made to files in a repository. Git checkout is a command used to switch branches or restore files to a previous version, but it will not remove modifications that have been made to files.
