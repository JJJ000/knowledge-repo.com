---
title: Setting up git to use ssh for authentication once
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Configure SSH keys to authenticate with the server, so that you don`t need to enter your credentials each time.
---

**Contents**

[TOC]

# Section 1: Generate an SSH Key
1. Open a terminal window.
2. Enter the command `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`.
3. Enter a file in which to save the key (e.g. `/Users/you/.ssh/id_rsa`).
4. Enter a passphrase.

# Section 2: Add SSH Key to SSH-Agent
1. Start the ssh-agent in the background.
2. Enter the command `eval $(ssh-agent -s)`.
3. Add your SSH private key to the ssh-agent.
4. Enter the command `ssh-add ~/.ssh/id_rsa`.

# Section 3: Add SSH Key to Github Account
1. Go to your Github Account Settings.
2. Select SSH and GPG Keys.
3. Click the New SSH Key button.
4. Enter a title for the key (e.g. "My Computer").
5. Paste your SSH key into the Key field.
6. Click the Add SSH Key button.

# Section 4: Configure Git to Use SSH
1. Open a terminal window.
2. Enter the command `git config --global user.name "Your Name"`.
3. Enter the command `git config --global user.email "your_email@example.com"`.
4. Enter the command `git config --global url."git@github.com:".insteadOf "https://github.com/"`.
