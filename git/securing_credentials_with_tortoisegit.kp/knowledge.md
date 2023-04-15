---
title: Tortoisegit stores user login information
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, TortoiseGit can save user authentication credentials for future use.
---

**Contents**

[TOC]

### Storing Credentials

TortoiseGit stores credentials in the Windows Credential Manager. This is a secure way to store and manage user credentials, and TortoiseGit uses it to store the credentials of the current user.

### Accessing Credentials

The credentials stored in the Windows Credential Manager can be accessed from the Windows Control Panel. From there, the user can view, edit, or delete the stored credentials.

### Encryption

The credentials stored in the Windows Credential Manager are encrypted using the Windows Data Protection API. This ensures that the credentials are secure and cannot be accessed by unauthorized users.

### Security

The Windows Credential Manager is a secure way to store user credentials, and TortoiseGit uses it to store the credentials of the current user. The credentials are encrypted using the Windows Data Protection API, and the user can access, edit, or delete the stored credentials from the Windows Control Panel.
