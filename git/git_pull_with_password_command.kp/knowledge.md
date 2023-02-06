---
title: What is the command to use when performing a git pull with a password?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run the command `git pull <remote> <branch>`, followed by entering the password when prompted.
---

**Contents**

[TOC]

##### Step 1: Generate SSH Key
1. Generate an SSH key pair by running the command `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
2. Enter a file in which to save the key (e.g. /Users/you/.ssh/id_rsa)
3. Enter a passphrase when prompted

##### Step 2: Add SSH Key to SSH Agent
1. Start the SSH agent in the background by running the command `eval $(ssh-agent -s)`
2. Add your SSH key to the SSH agent by running the command `ssh-add ~/.ssh/id_rsa`

##### Step 3: Add SSH Key to GitHub Account
1. Copy the SSH key to your clipboard by running the command `pbcopy < ~/.ssh/id_rsa.pub`
2. Go to your GitHub account settings and add the SSH key

##### Step 4: Pull Repository with Password
1. Run the command `git pull git@github.com:username/repository.git`
2. Enter the passphrase when prompted
