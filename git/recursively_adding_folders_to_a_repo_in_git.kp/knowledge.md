---
title: Add all the contents of the folder and its subfolders to the repository recursively
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: In order to add an entire folder to a repository in Git, use the command `git add -A` to recursively add all files and folders.
---

**Contents**

[TOC]

1. Create a New Repository

- Create a new repository on your local machine or on a remote hosting service such as GitHub, GitLab, or Bitbucket.

2. Add the Folder to the Repository

- Navigate to the folder you want to add to the repository and run the command `git init` to initialize the repository.

- Add the files to the repository by running the command `git add .`

3. Commit the Changes

- Commit the changes to the repository by running the command `git commit -m "Initial commit"`

4. Push the Changes

- Push the changes to the remote repository by running the command `git push origin master`
