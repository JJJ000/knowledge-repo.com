---
title: What is the command to specify the private ssh-key to use when running a shell command on git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Specify the path to the private SSH-key with the `-i` flag when running the git command.
---

**Contents**

[TOC]

### Generating a New SSH Key
1. Open Git Bash.
2. Type `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` and press enter.
3. Enter a file in which to save the key.
4. Enter a passphrase when prompted.

### Adding the SSH Key to the SSH Agent
1. Start the ssh-agent in the background by typing `eval $(ssh-agent -s)` and press enter.
2. Add your SSH key to the ssh-agent by typing `ssh-add ~/.ssh/id_rsa` and press enter.

### Adding the SSH Key to Your GitHub Account
1. Copy the SSH key to your clipboard by typing `clip < ~/.ssh/id_rsa.pub` and press enter.
2. Go to your GitHub Settings page.
3. Click on the SSH and GPG keys tab.
4. Click on the New SSH key button.
5. Paste the SSH key into the Key field.
6. Enter a descriptive title into the Title field.
7. Click on the Add SSH key button.

### Testing the Connection
1. Open Git Bash.
2. Type `ssh -T git@github.com` and press enter.
3. Type `yes` and press enter.
4. You should see a message saying "You've successfully authenticated, but GitHub does not provide shell access."
