---
title: How can I turn off the verification of ssl certificates in Python requests?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can disable the security certificate check in Python requests by setting the `verify` parameter to False.
---

**Contents**

[TOC]

1. **Disable Certificate Verification:**

To disable the certificate verification, you can set the verify parameter of the request to False.

```python
requests.get(url, verify=False)
```

2. **Disable Hostname Verification:**

To disable the hostname verification, you can set the verify parameter of the request to False and set the verify parameter of the SSLContext to None.

```python
import ssl

context = ssl.SSLContext()
context.verify_mode = ssl.CERT_NONE

requests.get(url, verify=False, context=context)
```

3. **Disable Certificate Verification and Hostname Verification:**

To disable both the certificate and hostname verification, you can set the verify parameter of the request to False and set the verify parameter of the SSLContext to CERT_NONE.

```python
import ssl

context = ssl.SSLContext()
context.verify_mode = ssl.CERT_NONE

requests.get(url, verify=False, context=context)
```

4. **Disable Certificate Verification for Specific URLs:**

If you want to disable certificate verification for specific URLs, you can use the verify parameter of the request and set it to a list of URLs for which you want to disable certificate verification.

```python
requests.get(url, verify=['url1', 'url2'])
```
