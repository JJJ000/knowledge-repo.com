---
title: Disable the insecurerequestwarning for unverified https requests in python2.6
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use `urllib2.HTTPSHandler(context=ssl.SSLContext(ssl.PROTOCOL\_TLSv1))` when making the request.
---

**Contents**

[TOC]

# Solution

## Using urllib2

The InsecureRequestWarning can be suppressed in Python2.6 by using the `urllib2` module. To do this, add the following code to the beginning of the script:

```python
import urllib2
urllib2.install_opener(urllib2.build_opener(urllib2.HTTPSHandler(
    context=ssl.SSLContext(ssl.PROTOCOL_TLSv1))))
```

This will disable the warning and allow the script to run without any issues.

## Using requests

The InsecureRequestWarning can also be suppressed in Python2.6 by using the `requests` library. To do this, add the following code to the beginning of the script:

```python
import requests
from requests.packages.urllib3.exceptions import InsecureRequestWarning
requests.packages.urllib3.disable_warnings(InsecureRequestWarning)
```

This will disable the warning and allow the script to run without any issues.
