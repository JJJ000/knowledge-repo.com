---
title: Git is giving a warning that the host has been added to the list of known hosts permanently
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git is warning that the remote host has been added to the list of known hosts and the connection is now secure.
---

**Contents**

[TOC]

#What is the Warning?
The warning "Warning: Permanently added to the list of known hosts" is displayed when a user connects to a remote server using SSH (Secure Shell). When a user connects to a remote server for the first time, the server's SSH host key is stored in the user's local SSH known_hosts file. This warning indicates that the host key has been successfully added to the user's local known_hosts file.

#What is an SSH Host Key?
An SSH host key is a cryptographic key used to identify a remote server. It is used to authenticate the server when a user connects to it. The host key is generated when the server is first set up and should not be changed.

#Why is it Important?
The purpose of the SSH host key is to ensure that the user is connecting to the correct server. If the host key is changed, it could indicate that the server has been compromised and the user should not continue the connection. By saving the host key in the user's local known_hosts file, the user can be sure that the server is the same one they connected to previously.

#What to Do if the Warning Appears?
If the warning "Warning: Permanently added to the list of known hosts" appears, it is usually safe to continue the connection. However, if the user suspects that the server has been compromised, they should not continue the connection and should contact the server administrator.
