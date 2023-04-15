---
title: Git cannot use the 'https' protocol
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git does not support the `https` protocol for remote operations.
---

**Contents**

[TOC]

### Overview

Git is a version control system that allows users to track changes in their code over time. It is an essential tool for developers to collaborate on projects and keep track of changes. When attempting to clone a repository, it is possible to encounter the error message "fatal: protocol 'https' is not supported". This error message indicates that the protocol being used to access the repository is not supported by the version of Git being used. 

### Causes

This error message is caused by attempting to clone a repository with an unsupported protocol. Protocols such as HTTP, HTTPS, and SSH are commonly used to access repositories. If the protocol being used is not supported by the version of Git being used, this error message will be displayed. 

### Solutions

The most common solution to this error message is to upgrade the version of Git being used. Upgrading to the latest version of Git will ensure that all protocols are supported. Additionally, it is possible to use an alternate protocol if the one being used is not supported. For example, if HTTPS is not supported, SSH can be used instead. Finally, it is possible to configure the version of Git being used to support the protocol being used. This can be done by editing the configuration file for Git.
