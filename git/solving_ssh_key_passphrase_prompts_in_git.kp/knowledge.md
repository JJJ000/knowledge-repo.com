---
title: I am continually being prompted for my ssh key passphrase when using git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Your SSH key passphrase is used to authenticate your connection to the remote server.
---

**Contents**

[TOC]

### SSH Key Passphrase

### What is an SSH Key Passphrase
An SSH key passphrase is a form of authentication that is used to grant access to an SSH key. It is a secret phrase or string of characters that is used to protect the private key associated with an SSH key pair.

### Why is Git Asking for the Passphrase
Git is asking for the passphrase because it is a security measure that helps to protect the private key associated with the SSH key pair. When a user attempts to access the private key, they must provide the passphrase to prove that they are authorized to do so.

### How to Set Up a Passphrase
Setting up a passphrase for an SSH key is simple. First, generate an SSH key pair using the `ssh-keygen` command. Then, provide a passphrase when prompted.

### How to Store the Passphrase
Once the passphrase has been set up, it is important to store it securely. It is recommended to store the passphrase in an encrypted file or password manager.
