---
title: The process of constructing the pkix path failed" and "no valid certificate chain could be found leading to the requested destination
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: These errors indicate that the Java application is unable to find a valid certificate chain for the requested target.
---

**Contents**

[TOC]

### Overview 
PKIX path building failed and unable to find valid certification path to requested target are two common errors that occur in Java when attempting to establish a secure connection. These errors indicate that the application failed to build a valid certificate chain from a trusted root certificate to the requested target.

### Causes 
These errors are usually caused by either a missing or an invalid certificate in the certificate chain. This can occur if the server is using an untrusted or self-signed certificate, or if the certificate is not trusted by the client. It can also occur if the certificate chain is incomplete or if the root certificate is not installed on the client.

### Solutions
The first step to resolving these errors is to ensure that the certificate chain is complete and valid. If the server is using a self-signed certificate, then the root certificate must be installed on the client in order to trust it. If the certificate chain is incomplete, then the missing certificates must be added.

To prevent these errors from occurring in the future, it is important to ensure that the server is using valid and trusted certificates. Additionally, the root certificate should be installed on the client to ensure that it is trusted.
