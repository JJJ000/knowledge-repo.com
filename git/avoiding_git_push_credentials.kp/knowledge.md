---
title: What is the best way to prevent having to enter my username and password every time I perform a git push?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can configure your username and password in the git configuration file and use the `git push` command without specifying the username and password.
---

**Contents**

[TOC]

### Setting Up SSH
1. Generate a SSH key pair on your computer. This can be done using the `ssh-keygen` command.
2. Add the public key to your remote repository. This can be done by copying the public key to the remote repository's SSH settings.

### Setting Up Git
1. Configure the remote repository URL to use the SSH protocol. This can be done using the `git remote set-url` command.
2. Configure Git to use the SSH key. This can be done by setting the `GIT_SSH_COMMAND` environment variable.

### Setting Up Credential Helper
1. Install the Git Credential Helper. This can be done using the `git config --global credential.helper` command.
2. Configure the Credential Helper to use the SSH key. This can be done by setting the `GIT_SSH_COMMAND` environment variable.
