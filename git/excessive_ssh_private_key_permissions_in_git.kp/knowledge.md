---
title: The permissions of an ssh private key when using git gui or ssh-keygen are set too widely
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, the SSH Private Key Permissions are set correctly by Git GUI or ssh-keygen.
---

**Contents**

[TOC]

# Section 1: Git GUI

When using Git GUI to create SSH keys, it is possible to set the permissions on the private key too wide. By default, the private key will be set to 0600, which means it can be read and written by the user who created the key. This is too open, as it means anyone who has access to the user's computer can read the private key, which could be used to gain access to the user's remote repositories.

# Section 2: ssh-keygen

When using ssh-keygen to create SSH keys, the default permissions for the private key are set to 0400. This means that only the user who created the key can read it, which is much more secure than the 0600 permissions of Git GUI. However, it is still possible to set the permissions too wide, as ssh-keygen allows the user to set the permissions to 0600.

# Section 3: Recommended Permissions

The recommended permissions for SSH private keys are 0400, which can be set using both Git GUI and ssh-keygen. This means that only the user who created the key can read it, which is the most secure option.

# Section 4: Conclusion

When creating SSH keys, it is important to be aware of the permissions that are set on the private key. Git GUI and ssh-keygen both allow the user to set the permissions too wide, which could lead to the private key being compromised. The recommended permissions for SSH private keys are 0400, which can be set using both Git GUI and ssh-keygen.
