---
title: The plugin for authentication, 'caching_sha2_password', is unsupported
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Python`s MySQL Connector/Python library does not support authentication plugin `caching\_sha2\_password`.
---

**Contents**

[TOC]

## What is 'caching_sha2_password' authentication plugin?

MySQL introduced the `caching_sha2_password` authentication plugin in version 8.0. This plugin provides a more secure authentication method compared to the older `mysql_native_password` plugin. When a user logs in using this plugin, the server sends a challenge to the client, and the client responds with a hashed password. The server then compares the hashed password with the stored hash in the password table to authenticate the user.

## Why 'caching_sha2_password' plugin is not supported in Python?

The 'caching_sha2_password' authentication plugin is not supported in Python because it requires a newer version of the `pymysql` library than what is presently available. The `pymysql` library, which is one of the most widely used libraries for Python to connect and interact with MySQL databases, does not support this authentication plugin.

## What is the solution for using 'caching_sha2_password' plugin in Python?

One solution for using the `caching_sha2_password` plugin in Python is to upgrade the `pymysql` library to a version that supports it. Currently, the latest version of `pymysql` (1.0.2) supports the `caching_sha2_password` plugin.

Alternatively, one could switch to using a different library that supports the `caching_sha2_password` plugin, such as `MySQL Connector/Python`. This library is an official Oracle-supported library for Python and supports the `caching_sha2_password` plugin.

## Conclusion

The `caching_sha2_password` authentication plugin is a more secure authentication method introduced in MySQL version 8.0, but it requires a newer version of the `pymysql` library than what is presently available. Upgrading to the latest version of `pymysql` or switching to a different library that supports this plugin, such as `MySQL Connector/Python`, may be necessary to use it.
