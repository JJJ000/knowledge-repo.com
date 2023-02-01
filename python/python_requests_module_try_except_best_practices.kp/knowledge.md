---
title: What is the proper syntax for using a try/except statement with the Python requests module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Try sending the request with the requests module, and catch any exceptions with a `except` block.
---

**Contents**

[TOC]

### Try Block

The following code snippet shows an example of how to use the `try` block when using the Python requests module:

```python
import requests

try:
    response = requests.get('http://example.com/')
    response.raise_for_status()
except requests.exceptions.HTTPError as err:
    print(err)
```

### Except Block

The following code snippet shows an example of how to use the `except` block when using the Python requests module:

```python
import requests

try:
    response = requests.get('http://example.com/')
    response.raise_for_status()
except requests.exceptions.HTTPError as err:
    print(err)
else:
    print('Request successful!')
```

### Finally Block

The following code snippet shows an example of how to use the `finally` block when using the Python requests module:

```python
import requests

try:
    response = requests.get('http://example.com/')
    response.raise_for_status()
except requests.exceptions.HTTPError as err:
    print(err)
else:
    print('Request successful!')
finally:
    print('Closing the connection.')
```
