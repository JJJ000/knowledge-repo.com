---
title: No host key type could be negotiated with 40.74.28.9 port 22. the offered key was ssh-rsa
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No SSH connection can be established, as the server`s host key type does not match the type supported by Git.
---

**Contents**

[TOC]

# Troubleshooting

## Understanding the Error

The error message “Unable to negotiate with 40.74.28.9 port 22: no matching host key type found. Their offer: ssh-rsa” is an indication that the host key type being offered by the server is not supported by the client. In this case, the server is offering an SSH-RSA key type, which is not supported by the client.

## Investigating the Host Key Type

In order to determine which host key type is supported by the client, it is necessary to investigate the host key type that is being offered by the server. This can be done by running the command `ssh -v 40.74.28.9` on the client machine. This will provide detailed information about the host key type being offered by the server.

## Resolving the Issue

Once the host key type being offered by the server is identified, it is necessary to configure the client to support that host key type. This can be done by editing the `~/.ssh/config` file on the client machine and adding an entry for the server’s host key type. For example, if the server is offering an SSH-RSA host key type, then the following entry should be added to the `~/.ssh/config` file:

```
Host 40.74.28.9
    HostKeyAlgorithms ssh-rsa
```

Once the configuration file is updated, the client should be able to successfully connect to the server.
