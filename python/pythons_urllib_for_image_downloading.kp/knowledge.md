---
title: Retrieving an image using python's urllib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can download a picture via urllib and Python by using the urlretrieve function from urllib.request module.
---

**Contents**

[TOC]

Downloading a Picture via urllib in Python

Python provides several libraries to download a picture from a URL. urllib is one such library used for this purpose. In the following sections, we will explore how to download a picture using urllib and Python.

Importing the urllib library
To use the urllib library, we need to import it in our Python script. Here is the syntax for importing the urllib library:

```python
import urllib.request
```

In this example, we imported the urllib.request module from the urllib library. This module helps us to download files from the internet.

Making a GET request
Now, to download a picture, we need to make an HTTP GET Request. We will use the urllib.request.urlretrieve() function to download the image. 

```python
urllib.request.urlretrieve(url, filename)
```

The url parameter is the URL of the picture we want to download, and the filename parameter is the file name that we will use to save the downloaded image. Here is an example:

```python
import urllib.request

url = 'https://example.com/image.jpg'
filename = 'image.jpg'

urllib.request.urlretrieve(url, filename)
```

In this example, we downloaded the image.jpg from the https://example.com URL.

Checking Download
After the download, we can check if the image is downloaded successfully or not using the following code block:

```python
import os

if os.path.exists(filename):
    print("File downloaded successfully!")
else:
    print("File download failed.")
```

This code block checks if the file exists in the current directory or not. If the file exists, it means that the download is successful. Otherwise, the download has failed.

Summary
In summary, we learned how to download a picture via urllib and Python. We imported the urllib library, made a GET request for the image, and saved it to a file. Finally, we checked if the download was successful or not.
