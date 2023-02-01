---
title: Retrieve a large file using Python and the requests library
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the requests library`s iter\_content() method to download large files in chunks.
---

**Contents**

[TOC]

# Section 1: Downloading the File

The easiest way to download a large file with `requests` is to use the `stream` parameter. This will allow us to stream the content directly to the file, without having to store it in memory first.

```python
import requests

url = 'https://example.com/large_file.zip'

r = requests.get(url, stream=True)

with open('large_file.zip', 'wb') as f:
    for chunk in r.iter_content(chunk_size=1024):
        if chunk:
            f.write(chunk)
```

# Section 2: Progress Bar

If you want to display a progress bar while downloading the file, you can use the `tqdm` library. This library provides a progress bar that can be used with any iterable.

```python
from tqdm import tqdm

url = 'https://example.com/large_file.zip'

r = requests.get(url, stream=True)

with open('large_file.zip', 'wb') as f:
    total_length = int(r.headers.get('content-length'))
    for chunk in tqdm(r.iter_content(chunk_size=1024), total=total_length//1024, unit="KB"):
        if chunk:
            f.write(chunk)
```

# Section 3: Resuming Download

If you need to resume a download, you can use the `headers` parameter to send the `Range` header. This will tell the server to send only the data that is not already downloaded.

```python
import os

url = 'https://example.com/large_file.zip'

if os.path.exists('large_file.zip'):
    # get the size of the downloaded file
    downloaded_size = os.path.getsize('large_file.zip')
    # set the `Range` header to resume the download
    headers = {'Range': 'bytes=%s-' % downloaded_size}
else:
    # start from the beginning
    headers = {}

r = requests.get(url, stream=True, headers=headers)

with open('large_file.zip', 'ab') as f:
    for chunk in r.iter_content(chunk_size=1024):
        if chunk:
            f.write(chunk)
```

# Section 4: Timeout

To prevent the download from taking too long, you can set a timeout. This will raise an exception if the download takes longer than the specified time.

```python
url = 'https://example.com/large_file.zip'

r = requests.get(url, stream=True, timeout=60)

with open('large_file.zip', 'wb') as f:
    for chunk in r.iter_content(chunk_size=1024):
        if chunk:
            f.write(chunk)
```
