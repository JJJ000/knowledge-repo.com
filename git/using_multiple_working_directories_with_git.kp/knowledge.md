---
title: What is the best way to set up multiple working directories using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can have multiple working directories with Git by creating multiple local repositories and cloning them from a remote repository.
---

**Contents**

[TOC]

### Setting up Multiple Working Directories

Git allows you to set up multiple working directories for each repository. This can be done by using the `git worktree` command. The `git worktree` command allows you to create a new working directory from the same repository. This new working directory is linked to the original repository, and any changes made in either directory will be reflected in the other. 

### Cloning the Repository

The first step in setting up multiple working directories is to clone the repository. This can be done by using the `git clone` command. This will create a copy of the repository in a new directory. 

### Creating the New Working Directory

Once the repository has been cloned, the new working directory can be created. This can be done by using the `git worktree add` command. This command will create a new working directory in the same repository as the original directory. 

### Managing Multiple Working Directories

Once the new working directory has been created, it can be managed like any other working directory. This includes committing changes, pushing to remote repositories, and pulling from remote repositories. It is important to note that any changes made in either directory will be reflected in both directories.
