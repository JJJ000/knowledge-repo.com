---
title: Duplicate a personal repository (github)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To clone a private repository on Github, you must have the appropriate permissions and use the `git clone` command with the repository`s HTTPS or SSH URL.
---

**Contents**

[TOC]

### 1. Create a Local Copy of the Repository

1. Open Git Bash.
2. Change the current working directory to the location where you want the cloned directory to be made.
3. Type `git clone` followed by the clone URL of the repository you want to clone.
4. Press Enter. Your local clone will be created.

### 2. Add the Remote Repository

1. Change the current working directory to the local repository you just created.
2. Type `git remote add` followed by the name you want to give the remote repository and the clone URL.
3. Press Enter. The remote repository will be added.

### 3. Fetch the Data from the Remote Repository

1. Change the current working directory to the local repository.
2. Type `git fetch` followed by the name of the remote repository.
3. Press Enter. The data from the remote repository will be fetched.

### 4. Pull the Data from the Remote Repository

1. Change the current working directory to the local repository.
2. Type `git pull` followed by the name of the remote repository.
3. Press Enter. The data from the remote repository will be pulled.
