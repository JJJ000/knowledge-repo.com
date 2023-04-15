---
title: What username and password do I need to provide when running "git clone git@remote.git"?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You cannot provide a username and password when running `git clone git@remote.git`; instead, you must use SSH keys to authenticate.
---

**Contents**

[TOC]

### SSH Keys
1. Generate an SSH key pair with `ssh-keygen -t rsa`
2. Copy the public key to the remote server with `ssh-copy-id user@remote`

### Configure Git
1. Configure the remote URL for the repository with `git config remote.origin.url git@remote:repo.git`
2. Set the username and password with `git config remote.origin.url username:password`

### Clone the Repository
1. Clone the repository with `git clone git@remote:repo.git`
2. Enter the username and password when prompted
