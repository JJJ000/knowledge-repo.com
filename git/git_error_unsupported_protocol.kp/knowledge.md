---
title: Git fatal error protocol 'http' not supported
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git does not support the `http` protocol.
---

**Contents**

[TOC]

### Overview
Git is a version control system that is used to track changes in source code over time. It is used by developers to keep track of their code and collaborate with other developers. The most common protocol used by Git is the Secure Shell (SSH) protocol, which is used to securely transfer data between two computers. However, Git can also be used with other protocols, such as HTTP.

### Error
When attempting to use Git with the HTTP protocol, the following error may be encountered:

`git: fatal: I don't handle protocol 'http'`

This error indicates that Git is not configured to use the HTTP protocol.

### Solution
To resolve this issue, the user must configure Git to use the HTTP protocol. This can be done by running the following command:

`git config --global http.sslVerify false`

This command will configure Git to use the HTTP protocol and disable SSL verification.

### Conclusion
Git can be used with the HTTP protocol, but it must be configured correctly. By running the command `git config --global http.sslVerify false`, the user can configure Git to use the HTTP protocol and resolve the error `git: fatal: I don't handle protocol 'http'`.
