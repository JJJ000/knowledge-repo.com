---
title: Configure git to fetch and push all branch repositories
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git config --global push.default current` to set up git to pull and push all branches.
---

**Contents**

[TOC]

### Set up git
1. Download and install git from [here](https://git-scm.com/).
2. Open a terminal window and run `git config --global user.name "<Your Name>"` to set your name in git.
3. Run `git config --global user.email "<Your Email>"` to set your email in git.

### Configure Remote Repository
1. Create a repository on GitHub.
2. Copy the repository URL.
3. Run `git remote add origin <repository URL>` to add the remote repository to your local git configuration.

### Pull All Branches
1. Run `git fetch --all` to fetch all branches from the remote repository.
2. Run `git pull --all` to pull all branches from the remote repository.

### Push All Branches
1. Run `git push --all` to push all branches to the remote repository.
