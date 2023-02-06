---
title: What is the distinction between running "git init" and "git init --bare"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: `git init` creates a new Git repository in the current directory, while `git init --bare` creates a new bare repository, which is a repository that doesn`t contain a working tree or a .git directory.
---

**Contents**

[TOC]

# Git Init
`git init` is used to create a new, local repository. It will create a new directory that contains all of the necessary Git metadata for the new repository. This command will also create a new `master` branch, which is the default branch for the repository.

# Git Init --Bare
`git init --bare` is used to create a new, remote repository. It will create a new directory that contains all of the necessary Git metadata for the new repository, but it will not create a new branch. This command is used to create a repository that will be used to store the "bare" version of the project, which is the version that is used for collaboration between multiple users.
