---
title: Suncertpathbuilderexception Java was unable to locate a valid certification path to the requested target
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: This error occurs when the system is unable to find a valid certificate chain to authenticate the requested target.
---

**Contents**

[TOC]

### Overview
Java's sun.security.provider.certpath.SunCertPathBuilderException is an exception that is thrown when the application is unable to find a valid certification path to the requested target.

### Cause
This exception is thrown when the application is unable to validate the certificate chain for the requested target. This can occur when the certificate chain is incomplete, or when the certificates in the chain are not trusted by the application. It can also occur when the certificate chain is not properly configured.

### Solutions
1. Ensure that the certificate chain is complete and valid.
2. Ensure that the certificates in the chain are trusted by the application.
3. Ensure that the certificate chain is properly configured.
