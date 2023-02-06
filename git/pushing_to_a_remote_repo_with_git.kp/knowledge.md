---
title: What is the process for pushing an initial commit to a remote repository using git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git push -u origin master` to push your local master branch to the remote origin repository.
---

**Contents**

[TOC]

# Step 1: Create a Remote Repository

The first step to doing an initial push to a remote repository with Git is to create a remote repository. This can be done on a hosting service such as GitHub, GitLab, or Bitbucket. Once the repository has been created, you will need to get the URL of the repository.

# Step 2: Initialize a Local Repository

The next step is to initialize a local repository on your computer. To do this, open up a terminal window and navigate to the directory where you want the repository to be located. Then run the command `git init` to create the repository.

# Step 3: Add Files to the Local Repository

Once the local repository has been initialized, you can add files to it. This can be done with the `git add` command followed by the file name or directory. For example, `git add myfile.txt` will add the file `myfile.txt` to the local repository.

# Step 4: Push to the Remote Repository

The final step is to push the local repository to the remote repository. To do this, you need to run the command `git push origin master`, where `origin` is the URL of the remote repository. This will push the local repository to the remote repository.
