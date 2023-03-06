---
title: Encountered an ssl certificate_verify_failed error while scraping http//en.wikipedia.org
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The error occurs because the request to http//en.wikipedia.org does not have a valid SSL certificate.
---

**Contents**

[TOC]

Section 1: Overview of SSL: CERTIFICATE_VERIFY_FAILED error

When working with web scraping or web crawling using Python, you may face an SSL: CERTIFICATE_VERIFY_FAILED error when accessing certain websites. This error occurs when Python is unable to verify the SSL certificate of the website you are trying to access. 

Section 2: Why does the SSL: CERTIFICATE_VERIFY_FAILED error occur for http://en.wikipedia.org in Python?

The SSL: CERTIFICATE_VERIFY_FAILED error may occur in Python when accessing the http://en.wikipedia.org website due to the following reasons:

- SSL certificate may not be valid or expired 
- Python's SSL library may not be able to access the appropriate CAs
- Firewall restrictions may prevent the SSL handshake process 

Section 3: How to fix the SSL: CERTIFICATE_VERIFY_FAILED error for http://en.wikipedia.org in Python?

To fix the SSL: CERTIFICATE_VERIFY_FAILED error for http://en.wikipedia.org in Python, you can try one or more of the following solutions:

- Ignore SSL verification by setting verify=False in the request parameters. However, this is not recommended for security reasons.
- Update the certificate file used by Python's SSL library. You can do this by pointing Python to the correct certificate file using the OS environment variable SSL_CERT_FILE.
- Disable system proxy settings by setting the environment variable HTTP_PROXY and HTTPS_PROXY to empty strings. 

Section 4: Example of how to fix the SSL: CERTIFICATE_VERIFY_FAILED error for http://en.wikipedia.org in Python

Here is an example code snippet that shows how to fix the SSL: CERTIFICATE_VERIFY_FAILED error for http://en.wikipedia.org in Python using the second solution mentioned above:

```
import ssl
import certifi
import urllib.request

ssl_context = ssl.create_default_context(cafile=certifi.where())
url = "http://en.wikipedia.org"
req = urllib.request.Request(url)
response = urllib.request.urlopen(req, context=ssl_context)
html = response.read().decode('utf-8')
print(html)
```

In this example, we are creating an SSL context with the updated certificate file from certifi library, and then using that to open the URL using Python's urrlib.request.urlopen() method. This should fix the SSL: CERTIFICATE_VERIFY_FAILED error for http://en.wikipedia.org in Python.
