---
title: Obtain dimensions of an image without having to load it into memory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use PIL`s Image module and its `open()` function with `verify=False` to get the image`s metadata without loading it into memory.
---

**Contents**

[TOC]

Section 1: Introduction

In certain cases, we may want to obtain the size of an image without actually loading the image into memory. This can be useful when dealing with large image files, where loading the entire file into memory can result in performance issues. In this article, we will explore various methods for obtaining the size of an image without loading it into memory.

Section 2: Using the Pillow Library

The Pillow library (a fork of the Python Imaging Library) provides a convenient method for obtaining the size of an image without loading it into memory. Here's an example of how to use Pillow to get the size of an image:

```python
from PIL import Image

with Image.open('path/to/image.jpg') as img:
    width, height = img.size
    print(f"Image size: {width} x {height}")
```

In the above code, we open the image file using the `Image.open()` method, which returns a `Image` object. We then extract the image size using the `.size` attribute of the `Image` object. Since we're using a context manager (`with` statement), the image is automatically closed when we exit the context, which helps ensure that we don't keep the file open longer than necessary.

Section 3: Using the imghdr Library

The imghdr library provides support for determining the type of an image file, in addition to its size. Here's an example of how to use imghdr to get the size of an image:

```python
import imghdr

def get_image_size(filepath):
    with open(filepath, 'rb') as img_file:
        header = img_file.read(24)
        size = imghdr.tests.get_image_size(header)
        return size

file_path = 'path/to/image.jpg'
image_size = get_image_size(file_path)

if image_size is not None:
    print(f"Image size: {image_size[0]} x {image_size[1]}")
else:
    print("Image file not found or is not a valid image file.")
```

In the above code, we define a `get_image_size()` function that takes the file path of an image as its parameter. We then read the first 24 bytes of the image file using the built-in `open()` function with the `'rb'` flag (read mode for binary files). We pass this header to the `get_image_size()` function provided by the imghdr library, which returns a tuple containing the width and height of the image (in pixels). If imghdr is unable to determine the dimensions of the image (e.g. the file is not a valid image file), it returns `None`.

Section 4: Using the Wand Library

The Wand library is another Python library for working with image files, and it provides a convenient method for obtaining the size of an image without loading it into memory. Here's an example of how to use Wand to get the size of an image:

```python
from wand.image import Image

with Image(filename='path/to/image.jpg') as img:
    width, height = img.size
    print(f"Image size: {width} x {height}")
```

In the above code, we open the image file using the `Image()` constructor, passing the filename as its parameter. We again use a context manager (`with` statement) to ensure that the image file is closed when we exit the context. We then extract the image size using the `.size` attribute of the `Image` object.

Section 5: Conclusion

In this article, we explored various methods for obtaining the size of an image without loading it into memory. We saw how to use the Pillow, imghdr, and Wand libraries to obtain the image size, and learned about the different ways in which these libraries work. By using these techniques, we can more efficiently handle large image files in our Python programs.
