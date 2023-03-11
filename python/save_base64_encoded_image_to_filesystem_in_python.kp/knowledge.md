---
title: Transform base64 encoded string to an image format and store it onto the file system
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To convert a base64 string to an image and save it on the filesystem in Python, use the `base64` and `PIL` modules, decode the base64 string, initialize a `BytesIO` object, create a new `Image` object from the bytes and save it using the `save()` method.
---

**Contents**

[TOC]

1. Decoding Base64 String
To convert a base64 string to an image, the first step is to decode the base64 string. This can be done using the `base64` module in Python. Here's an example:

```python
import base64

# base64 string
base64_string = "data:image/jpeg;base64,/9j/4AAQSkZ..."

# decode base64 string
image_data = base64.b64decode(base64_string.split(",")[1])
```

The `split(",")[1]` is used to remove the image file type and metadata before decoding the base64 string.

2. Saving Image to Filesystem
Once the base64 string is decoded to image data, the next step is to save the image to the filesystem. This can be done using Python's `open` function and writing the image data to a file in binary mode. Here's an example:

```python
import base64

# base64 string
base64_string = "data:image/jpeg;base64,/9j/4AAQSkZ..."

# decode base64 string
image_data = base64.b64decode(base64_string.split(",")[1])

# save image
with open("image.jpg", "wb") as f:
    f.write(image_data)
```

The `with open` statement ensures that the file is automatically closed after writing.

3. Putting it All Together
Here's the full code to convert a base64 string to an image and save it to the filesystem:

```python
import base64

def save_base64_image(base64_string, filename):
    # decode base64 string
    image_data = base64.b64decode(base64_string.split(",")[1])

    # save image
    with open(filename, "wb") as f:
        f.write(image_data)
```

This function takes a base64 string and a filename and saves the image to the filesystem with the given filename.

4. Using the Function
Using the `save_base64_image` function is as simple as passing in the base64 string and filename:

```python
# base64 string
base64_string = "data:image/jpeg;base64,/9j/4AAQSkZ..."

# save image
save_base64_image(base64_string, "image.jpg")
```

This will save the image with filename "image.jpg" to the current directory.
