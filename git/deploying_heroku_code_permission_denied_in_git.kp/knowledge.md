---
title: The deployment of heroku code was not allowed due to publickey access being denied. the connection was unexpectedly terminated before completion
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: The SSH key used to authenticate the connection is not valid.
---

**Contents**

[TOC]

### Solution 1: Check SSH Keys

Ensure that the correct SSH keys are associated with the Heroku account. This can be done by running the command `heroku keys:add` from the command line.

### Solution 2: Generate a New SSH Key

If the SSH keys are not associated correctly, generate a new SSH key with the command `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` and add it to the Heroku account with the command `heroku keys:add`.

### Solution 3: Update the Git Config

Update the Git config to use the correct SSH key. This can be done by running the command `git config --global user.name "your_name"` and `git config --global user.email "your_email@example.com"`.

### Solution 4: Add the SSH Key to the SSH Agent

Add the SSH key to the SSH agent with the command `ssh-add ~/.ssh/id_rsa`. This will ensure that the correct SSH key is used when connecting to the Heroku server.
