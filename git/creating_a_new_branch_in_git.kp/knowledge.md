---
title: Creating a new branch with no files for a new project
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git checkout -b <new\_branch\_name>` to create a new empty branch for a new project in Git.
---

**Contents**

[TOC]

### Initializing a Local Repository
1. Create a directory for the project, e.g. `mkdir my-project`.
2. Change directory into the new project directory, e.g. `cd my-project`.
3. Initialize a local repository, e.g. `git init`.

### Creating a New Branch
1. Checkout a new branch, e.g. `git checkout -b my-project-branch`.
2. Add and commit any initial files to the branch, e.g. `git add . && git commit -m “Initial commit”`.

### Pushing the Branch to Remote
1. Create a new remote repository, e.g. `git remote add origin <remote-repo-url>`.
2. Push the new branch to the remote repository, e.g. `git push -u origin my-project-branch`.

### Verifying the Push
1. Check the remote repository to verify that the branch was pushed correctly, e.g. `git ls-remote origin`.
2. Verify that the branch is listed in the remote repository, e.g. `git branch -a`.
