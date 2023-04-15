---
title: What is the procedure for obtaining my ssh public key?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Your SSH public key can be accessed in Git by adding it to your SSH keys in your Git account settings.
---

**Contents**

[TOC]

### Section 1 - Generating an SSH Key
1. Open the terminal on your computer.
2. Type `ssh-keygen -t rsa` and press Enter.
3. Enter the file in which to save the key and press Enter.
4. Enter a passphrase and press Enter.

### Section 2 - Adding an SSH Key to the SSH Agent
1. Type `eval $(ssh-agent -s)` and press Enter.
2. Type `ssh-add ~/.ssh/id_rsa` and press Enter.

### Section 3 - Adding an SSH Key to GitHub
1. Log in to your GitHub account.
2. Go to Settings > SSH and GPG Keys.
3. Click New SSH Key.
4. Enter a title for the key and paste your public key into the Key field.
5. Click Add SSH Key.

### Section 4 - Testing the SSH Key
1. Open the terminal on your computer.
2. Type `ssh -T git@github.com` and press Enter.
3. Enter your passphrase and press Enter.
4. If the key is successfully added, you will see a message indicating that you have successfully authenticated.
