---
title: Getting an error message of "fatal not a git repository" when trying to connect to a git repository remotely
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You must first initialize a local repository before you can add a remote.
---

**Contents**

[TOC]

1. Check Your Current Working Directory
--------------------------------------
When you receive the error "fatal: Not a git repository", this usually means that the current working directory is not a Git repository. Before attempting to remote add a Git repo, check that you are in the correct working directory by using the `pwd` command. This will display the full path to your current working directory. 

2. Initialize the Repository
----------------------------
If the current working directory is not a Git repository, you will need to initialize it before attempting to remote add a Git repo. To do this, use the `git init` command. This will create a new Git repository in the current working directory. 

3. Add the Remote Repository
----------------------------
Once the repository has been initialized, you can add the remote repository using the `git remote add` command. This command takes two arguments: the name of the remote repository and the URL of the repository. For example, `git remote add origin https://github.com/username/repository.git`. 

4. Verify the Remote Repository
-------------------------------
Once the remote repository has been added, you can verify that it was added correctly by using the `git remote -v` command. This will display a list of all the remote repositories associated with the current working directory. If the remote repository was added correctly, it should appear in the list.
