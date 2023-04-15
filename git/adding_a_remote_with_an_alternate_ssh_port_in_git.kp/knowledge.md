---
title: Add a remote repository to git using a different ssh port
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, you can add a remote with an SSH port by using the command `git remote add <name> <url> -p <port>`.
---

**Contents**

[TOC]

### Setting Up SSH

In order to add a remote repository using a different SSH port, you will need to first set up your SSH configuration. This includes setting up an SSH key, configuring the SSH agent, and adding the necessary SSH port to the SSH config file.

### Generating an SSH Key

The first step is to generate an SSH key. This can be done by running the `ssh-keygen` command in the terminal. This will create a pair of public and private keys that will be used to authenticate with the remote repository.

### Configuring the SSH Agent

The next step is to configure the SSH agent. This is done by running the `ssh-agent` command in the terminal. This will start the SSH agent and allow it to manage your SSH keys.

### Adding the SSH Port to the SSH Config File

The last step is to add the necessary SSH port to the SSH config file. This is done by editing the `~/.ssh/config` file and adding the port number to the `Host` section. Once this is done, the remote repository can be added using the different SSH port.
