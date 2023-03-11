---
title: Unable to install Python packages due to an ssl error that reads 'tlsv1_alert_protocol_version'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: This error occurs when the Python package installation process attempts to use an outdated version of the TLS protocol.
---

**Contents**

[TOC]

Section 1: Introduction
When trying to install Python packages, sometimes an error can occur that is related to the SSL/TLS protocol version. This error message typically reads "SSL: TLSV1_ALERT_PROTOCOL_VERSION" and can prevent the installation of certain packages.

Section 2: Causes of the Error
The most common cause of the "SSL: TLSV1_ALERT_PROTOCOL_VERSION" error is an outdated version of OpenSSL. The TLS protocol has undergone several updates over the years, and some servers and clients only support the latest versions. When trying to connect to an outdated server using an old version of OpenSSL, the connection might be refused, resulting in the "TLSV1_ALERT_PROTOCOL_VERSION" error message.

Section 3: Possible Solutions
The easiest solution to this problem is to update OpenSSL to the latest version. This can be done by downloading and installing the latest version of the OpenSSL library from the official website.

Another possible solution is to force the installation of the package by setting the "ssl" module to use TLSv1.2 instead of the default TLSv1.0. This can be done by adding the following line of code at the beginning of the Python script:

import os
os.environ['PYTHONHTTPSVERIFY'] = '0'
os.environ['HTTPS_PROTOCOL'] = 'TLSv1.2'

This code sets the "PYTHONHTTPSVERIFY" and "HTTPS_PROTOCOL" environment variables to force Python to use TLSv1.2.

Section 4: Conclusion
The "SSL: TLSV1_ALERT_PROTOCOL_VERSION" error can be caused by an outdated version of OpenSSL or an outdated TLS protocol version. Updating OpenSSL to the latest version and forcing the use of TLSv1.2 can help resolve this issue. If these solutions do not work, it may be necessary to contact the package maintainers or server administrators for further assistance.
