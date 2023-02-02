---
title: Retrieve a file from the internet using Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the `urllib.request` module to download a file from a web URL in Python 3.
---

**Contents**

[TOC]

# Section 1: Import Libraries

In order to download a file from the web, we will need to import the `requests` library.

```python
import requests
```

# Section 2: Download File

Using the `requests` library, we can download a file from the web by using the `get` method.

```python
url = 'http://example.com/file.pdf'
r = requests.get(url)
```

# Section 3: Save File

Once we have downloaded the file, we can save it to our local machine by using the `write` method.

```python
with open('file.pdf', 'wb') as f:
    f.write(r.content)
```

# Section 4: Verify File

Once the file has been saved, we can verify that the file was downloaded correctly by using the `status_code` attribute.

```python
if r.status_code == 200:
    print('File successfully downloaded!')
```
