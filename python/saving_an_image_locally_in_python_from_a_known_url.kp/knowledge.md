---
title: What is the method to locally store an image with Python when I am already aware of its url address?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `urllib` module to download the image from the URL and save it to a local file using the `open()` and `write()` functions.
---

**Contents**

[TOC]

## Import Required Libraries

The first step is to import the necessary libraries. In this example, we need to import the urllib.request library for handling HTTP requests and the shutil library for saving the image locally.

```python
import urllib.request
import shutil
```

## Retrieve Image from URL

We can use the `urllib.request.urlretrieve()` method to retrieve the image from the specified URL address. This method takes two arguments - the URL of the image and the local file path where we want to save the image. 

```python
url = "https://example.com/image.jpg"
file_path = "/path/to/save/image.jpg"

urllib.request.urlretrieve(url, file_path)
```

## Save Image Locally

Finally, we can use the `shutil.copyfile()` method to save the image locally. This method takes two arguments - the source path (i.e., the path to the downloaded image) and the destination path (i.e., the path where we want to save the image locally).

```python
source_path = "/tmp/image.jpg"
destination_path = "/path/to/save/image.jpg"

shutil.copyfile(source_path, destination_path)
```

## Complete Example

Putting it all together, the complete Python code to save an image locally from a given URL address can be written as follows:

```python
import urllib.request
import shutil

url = "https://example.com/image.jpg"
download_path = "/tmp/image.jpg"
local_path = "/path/to/save/image.jpg"

# Download image from URL
urllib.request.urlretrieve(url, download_path)

# Save image locally
shutil.copyfile(download_path, local_path)
```
