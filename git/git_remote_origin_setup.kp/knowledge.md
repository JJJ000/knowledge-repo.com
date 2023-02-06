---
title: Establishing a git remote repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the command `git remote add origin <remote repository URL>` to set up a git remote origin.
---

**Contents**

[TOC]

##Step 1: Initialize a Local Repository

1. Create a directory to contain the project.
2. Go into the new directory.
3. Type `git init` to create a new local repository.

##Step 2: Add a Remote

1. In the terminal, type `git remote add origin <server>`, where `<server>` is the URL of the remote repository you are adding.

##Step 3: Push to the Remote

1. Type `git push -u origin master` to push the changes in your local repository up to the remote repository.

##Step 4: Verify the Remote

1. Type `git remote -v` to verify the new remote URL.
