---
title: Troubleshooting "ssl certificate_verify_failed" error with urllib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The `SSL CERTIFICATE\_VERIFY\_FAILED` error can be fixed by disabling certificate validation in urllib.
---

**Contents**

[TOC]

# Introduction

Python is a popular programming language used by many developers and data scientists. One of the modules that Python provides is `urllib`, which is used to make HTTP requests to web servers. However, when using `urllib`, users may encounter the error `SSL: CERTIFICATE_VERIFY_FAILED`. This error occurs when the server's SSL certificate cannot be verified.

# What is SSL?

Secure Sockets Layer (SSL) is a protocol that provides secure communication over the internet. It is used to encrypt data sent between two computers, such as when a user is accessing a website. SSL certificates are used to authenticate the identity of the server, and to ensure that the data is not intercepted by a third party.

# What is the SSL: CERTIFICATE_VERIFY_FAILED Error?

The SSL: CERTIFICATE_VERIFY_FAILED error occurs when the server's SSL certificate cannot be verified. This can happen for a variety of reasons, such as the certificate being expired or invalid, or the server's domain name not matching the certificate.

# How to Fix the SSL: CERTIFICATE_VERIFY_FAILED Error

The SSL: CERTIFICATE_VERIFY_FAILED error can be fixed by disabling the certificate verification in `urllib`. This can be done by setting the `REQUESTS_CA_BUNDLE` environment variable to `false`.

Alternatively, the server's SSL certificate can be updated to a valid one. This can be done by contacting the server's administrator.
