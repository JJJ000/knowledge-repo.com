---
title: How can I access git// protocol when it is blocked by my company?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use a different protocol such as HTTPS or SSH.
---

**Contents**

[TOC]

## Use a Different Protocol

If your company is blocking the git:// protocol, you can try using a different protocol such as HTTPS or SSH. To use HTTPS, you can clone a repository using the following command:

```
git clone https://github.com/username/repository.git
```

To use SSH, you can clone a repository using the following command:

```
git clone git@github.com:username/repository.git
```

## Use a Proxy

If you are unable to use a different protocol, you may be able to use a proxy to access the git:// protocol. You can use a tool such as corkscrew to tunnel through an HTTP proxy to access the git:// protocol.

## Use a VPN

If you are still unable to access the git:// protocol, you may be able to use a VPN to bypass the restrictions. You can download and install a VPN client on your computer and connect to a VPN server that is not blocked by your company. This will allow you to access the git:// protocol.
