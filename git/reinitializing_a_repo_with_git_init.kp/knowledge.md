---
title: What happens if you run 'git init' twice - will it create a new repository or reset an existing one?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Running git init twice will reinitialize an existing repository.
---

**Contents**

[TOC]

# Initializing a Repository
Running `git init` will initialize a repository, creating a `.git` folder in the current directory. This folder contains all of the necessary files for a Git repository.

# Re-Initializing an Existing Repository
Running `git init` on an existing repository will not reinitialize the repository. It will simply be ignored and no changes will be made.
