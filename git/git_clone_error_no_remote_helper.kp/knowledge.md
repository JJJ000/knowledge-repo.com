---
title: Git clone failed to locate a remote helper for 'https
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The remote helper for `https` is not installed correctly.
---

**Contents**

[TOC]

### Cause

The error occurs when attempting to clone a repository over HTTPS, but the system does not have the necessary library installed to support the connection. This is typically caused by an outdated version of Git, or by not having the necessary dependencies installed.

### Solution

The most common solution is to update Git to the latest version. This can be done by downloading the latest version from the official website, or by using a package manager such as apt-get or yum.

Once Git has been updated, it is important to ensure that the necessary libraries are installed to support HTTPS connections. This can be done by installing the appropriate packages for your system. For example, on a Debian-based system, the following command can be used to install the necessary dependencies:

```git
sudo apt-get install libcurl4-openssl-dev libssl-dev
```

Once the dependencies have been installed, the repository can be cloned using HTTPS.
