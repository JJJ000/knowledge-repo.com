---
title: How do .gitignore and .gitkeep differ?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: .gitignore is used to specify which files and directories should be ignored by Git, while .gitkeep is used to create an empty directory that will be tracked by Git.
---

**Contents**

[TOC]

### .gitignore

`.gitignore` is a file that tells git which files and directories to ignore when committing changes to a repository. It is used to prevent certain files from being added to the repository, such as compiled binaries, temporary files, and sensitive information.

### .gitkeep

`.gitkeep` is a placeholder file used to keep empty directories in a Git repository. It is used to prevent Git from deleting empty directories when committing changes. It is not necessary to commit `.gitkeep` files to the repository, but it is a good practice to do so.

### Differences

The main difference between `.gitignore` and `.gitkeep` is the purpose they serve. `.gitignore` is used to prevent files from being added to the repository, while `.gitkeep` is used to keep empty directories in the repository. Additionally, `.gitignore` is a required file in order for Git to ignore certain files, while `.gitkeep` is not required.
