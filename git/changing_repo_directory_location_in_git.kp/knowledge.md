---
title: Move the git repository to a different directory
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can change the Git repository directory location by running the `git config --local core.worktree` command.
---

**Contents**

[TOC]

### Cloning the Repository

Cloning a repository is the process of downloading a copy of a repository from a remote source, such as a server, to your local machine. To clone a repository, you will need to have Git installed on your local machine.

Once you have Git installed, you can clone a repository by running the `git clone` command followed by the repository URL. For example, to clone the repository at `https://github.com/user/repo.git`, you would run the command `git clone https://github.com/user/repo.git`. This will create a local copy of the repository in the current directory.

### Changing the Repository Directory

If you want to change the directory where the repository is stored, you can use the `git clone` command with the `--separate-git-dir` flag. This flag allows you to specify a different directory for the repository.

For example, if you want to clone the repository at `https://github.com/user/repo.git` to the directory `/home/user/repos/repo`, you would run the command `git clone --separate-git-dir=/home/user/repos/repo https://github.com/user/repo.git`. This will create a local copy of the repository in the specified directory.

### Verifying the Repository Directory

After cloning the repository, you can verify that the repository has been cloned to the correct directory by running the `git config --get core.bare` command. If the command returns `false`, then the repository has been cloned to the correct directory.

### Setting the Repository Directory

If you want to set the repository directory permanently, you can use the `git config` command with the `core.bare` flag. For example, to set the repository directory to `/home/user/repos/repo`, you would run the command `git config core.bare /home/user/repos/repo`. This will set the repository directory permanently.
