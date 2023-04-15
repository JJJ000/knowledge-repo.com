---
title: What is the best way to store a username and password in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You cannot save username and password in Git.
---

**Contents**

[TOC]

### Storing Credentials in Git Config

Git allows you to store your credentials in the git config file. To do this, run the following command:

```git
git config --global user.name "Your Name"
git config --global user.email "Your Email"
```

This will store your credentials in the global git config file.

### Using Credential Helpers

Git also provides the ability to store credentials in a "credential helper". This is a helper program that stores your credentials in a secure manner. To set up a credential helper, run the following command:

```git
git config --global credential.helper <helper-name>
```

Replace `<helper-name>` with the name of the credential helper you want to use.

### Using SSH Keys

Git also supports using SSH keys to authenticate with remote repositories. To generate an SSH key, run the following command:

```git
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

This will generate an SSH key pair that you can use to authenticate with remote repositories.

### Using Git Credential Managers

Finally, you can also use a Git credential manager to store your credentials in a secure manner. These are programs that store your credentials in an encrypted format and provide an interface for managing them. Popular credential managers include [Git Credential Manager for Windows](https://github.com/Microsoft/Git-Credential-Manager-for-Windows) and [Git Credential Manager for Mac OS X](https://github.com/microsoft/Git-Credential-Manager-for-Mac-OS-X).
