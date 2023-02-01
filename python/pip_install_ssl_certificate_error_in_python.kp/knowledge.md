---
title: The 'pip install' command is not working due to an ssl certificate verification error "[ssl certificate_verify_failed] certificate verify failed (_ssl.c598)"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: This error can be resolved by running the command `python -m pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org <package>`.
---

**Contents**

[TOC]

### Introduction
When attempting to install a package using `pip`, an error may occur stating `connection error: [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:598)`. This error occurs when the SSL certificate of the website hosting the package is not properly verified.

### Causes
The cause of this error is that the root certificates of the website hosting the package are not properly verified by the Python installation. This can be due to the root certificates not being installed on the system, or the certificates may have expired.

### Solutions
The following solutions can be used to resolve the `connection error: [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:598)` error:

1. Install the root certificates of the website hosting the package.
2. Update the Python installation to the latest version.
3. Disable SSL verification when using `pip` by using the `--trusted-host` option.
4. Set the `PIP_TLS_REJECT_UNAUTHORIZED` environment variable to `0`.
