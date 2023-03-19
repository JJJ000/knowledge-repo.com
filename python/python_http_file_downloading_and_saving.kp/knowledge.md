---
title: How can files be downloaded via http and saved to disk in Python at a basic level?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the urllib library in Python to download the HTTP file and save it to disk using the open function with write binary mode.
---

**Contents**

[TOC]

# 1. Using the requests library to download files

One of the easiest ways to download a file from a URL in Python is by using the requests library. This library is an HTTP library that allows us to send HTTP/1.1 requests extremely easily. Here's an example of how to download an image file using requests:

```python
import requests

url = 'https://example.com/image.jpg'
response = requests.get(url)

with open('image.jpg', 'wb') as file:
    file.write(response.content)
```

In this code snippet, we first import the requests library. We then define the URL of the file we want to download. We use the `get` method of the requests library to send an HTTP GET request to the server and retrieve the file. Then, we open a new file `"image.jpg"` in write binary mode `'wb'` and write the content of the response to this file. The `content` attribute of the response object is a bytes object that contains the response body.

# 2. Using the urllib library to download files

Another way to download files in Python is to use the urllib library. This library comes pre-installed with Python and provides a simple interface to work with URLs. Here's how you can use urllib to download a file:

```python
import urllib.request

url = 'https://example.com/image.jpg'

urllib.request.urlretrieve(url, 'image.jpg')
```

Here, we import the `urllib.request` module and define the URL of the file we want to download. We then use the `urlretrieve` function of the module to download the file and save it to the specified path `"image.jpg"`. The `urlretrieve` function is a simple way of downloading files, but it does not provide the same level of control as the requests library.

# 3. Using the wget library to download files

The wget library is another way to download files in Python. This library provides a higher-level interface compared to urllib, making it easier to work with URLs. Here's how you can use wget to download a file:

```python
import wget

url = 'https://example.com/image.jpg'

filename = wget.download(url)
```

In this code snippet, we first import the `wget` module and define the URL of the file we want to download. We then use the `download` function of the `wget` module to download the file and store it as `"filename"` in the current directory. The `download` function returns the filename of the downloaded file, which we can use for further processing.

# 4. Error handling and exceptions

When downloading files, it's important to handle errors and exceptions gracefully. Here's an example of how we can wrap the code for downloading files in a try-except block to catch errors:

```python
import requests

url = 'https://example.com/image.jpg'

try:
    response = requests.get(url)
    response.raise_for_status()
except requests.exceptions.HTTPError as err:
    print(f'HTTP error: {err}')
except Exception as err:
    print(f'Other error occurred: {err}')
else:
    with open('image.jpg', 'wb') as file:
        file.write(response.content)
```

In this code snippet, we first define the URL of the file we want to download. Then, we use a try-except block to try to download the file using the requests library. If an HTTP error occurs, we catch it and print an error message. If any other exception occurs, we catch it and print a generic error message. If no errors occur, we open a new file `"image.jpg"` in write binary mode and write the content of the response to this file. This way, even if an error occurs during the download, we can handle it and continue execution of our program.
