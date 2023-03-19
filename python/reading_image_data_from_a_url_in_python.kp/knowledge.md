---
title: What is the method to extract image data from a url?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use the Python Imaging Library (PIL) module to read image data from a URL in Python using the open() function.
---

**Contents**

[TOC]

## Import Necessary Libraries
The very first section of solving the problem is the import of necessary libraries. 

Python provides to read image data from a URL which involves web-based image processing, we will need to use Python Imaging Library (PIL). So, we import the PIL library using the below statement.

```python
from PIL import Image
from urllib.request import urlopen
```


## Read Image Data from URL
Once the necessary libraries have been imported, we can easily read image data from a URL. We will achieve this by following the below steps -

- First of all, we need to open a connection to the URL.
- Then, we can use PIL functionality to read the data from the image URL.
- Finally, the image content will be decoded and returned.

Below is the code snippet to read image data from URL.

```python
from PIL import Image
from urllib.request import urlopen

image_url = "https://example.com/image.jpg"
image_content = urlopen(image_url).read()
image_file = BytesIO(image_content)
im = Image.open(image_file)
im.show()
```


## Display Image
Images can be very large and the data that comes from a URL is just a chunk of the file, so we will probably want to display the image to make sure we are reading it correctly. 

We can achieve this by using PIL. Here is the code snippet to display the image.

```python
from PIL import Image
from urllib.request import urlopen

image_url = "https://example.com/image.jpg"
image_content = urlopen(image_url).read()
image_file = BytesIO(image_content)
im = Image.open(image_file)
im.show()
```

This code will display the image in a window. If the image does not open, try running these lines separately -

```python
from PIL import Image
from io import BytesIO
from urllib.request import urlopen

image_url = "https://example.com/image.jpg"
image_data = urlopen(image_url).read()
im = Image.open(io.BytesIO(image_data))
im.show()
```


## Summary
We can read image data from a URL in Python in just a few simple steps. We can use the Pillow library to read and display the image content. In the example code, we used urlopen() function first to open a connection to the URL and then used Pillow functionality to read the data from the URL content.
