---
title: How can I transfer ssh keypairs generated with puttygen (windows) to be used with ssh-agent and keychain (linux)?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can use the PuTTYgen tool to convert the PuTTY key pairs into OpenSSH format, which can then be used by ssh-agent and Keychain in Linux.
---

**Contents**

[TOC]

### Section 1 - Convert PuTTY Keypair to OpenSSH Format
1. Open PuTTYgen and select the keypair you wish to convert.
2. Click the `Conversions` menu and select `Export OpenSSH key`.
3. Save the keypair as a `.pem` file.

### Section 2 - Add Keypair to ssh-agent
1. Open the terminal and run the command `ssh-add <path-to-keypair>.pem`.
2. Enter the passphrase for the keypair.

### Section 3 - Add Keypair to Keychain
1. Run the command `ssh-add -K <path-to-keypair>.pem`.
2. Enter the passphrase for the keypair.

### Section 4 - Use Keypair with Git
1. Run the command `git config --global user.signingkey <path-to-keypair>.pem`.
2. Run the command `git config --global commit.gpgsign true`.
3. You can now use the keypair to sign your commits in Git.
