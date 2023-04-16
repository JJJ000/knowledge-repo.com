---
title: Urllib3 is unable to configure ssl correctly due to the absence of an authentic sslcontext object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: urllib3 is unable to configure SSL correctly without a true SSLContext object.
---

**Contents**

[TOC]

### What is InsecurePlatformWarning?
InsecurePlatformWarning is a warning issued by the urllib3 library when a true SSLContext object is not available. This warning is raised when the SSLContext object is not available and urllib3 is unable to configure SSL settings appropriately.

### Why is it Raised?
The warning is raised when the SSLContext object is not available, which means that urllib3 is unable to configure SSL settings appropriately. This can occur if the SSLContext object is not provided or if the version of Python being used does not support the SSLContext object.

### How to Fix it?
The warning can be fixed by providing a true SSLContext object or by upgrading the version of Python being used. It is important to ensure that the SSLContext object is configured correctly, as this will ensure that the SSL settings are configured properly.

### Conclusion
InsecurePlatformWarning is a warning issued by the urllib3 library when a true SSLContext object is not available. This warning can be fixed by providing a true SSLContext object or by upgrading the version of Python being used. It is important to ensure that the SSLContext object is configured correctly, as this will ensure that the SSL settings are configured properly.
