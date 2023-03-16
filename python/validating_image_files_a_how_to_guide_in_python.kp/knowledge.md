---
title: What is the method to determine if a file is a legitimate image file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You can check if a file is a valid image file in Python by using the Pillow library to try to open the file and catching any exceptions if the file cannot be opened.
---

**Contents**

[TOC]

## Introduction
Python provides several libraries for image processing, such as Pillow, OpenCV, and scikit-image. These libraries can be used to check whether a file is a valid image file or not. In this tutorial, we will explore how to use the Pillow library to perform this task.

## Installing Pillow
The first step is to install the Pillow library. You can install it using pip with the following command:

```
pip install Pillow
```

## Opening the Image
To check whether a file is a valid image file or not, we can try to open it using the Image module of the Pillow library. If the file can be opened and parsed as an image, then it is a valid image file; otherwise, an exception will be raised.

Here is an example code snippet that demonstrates how to do this:

``` python
from PIL import Image

try:
    with Image.open('path/to/image_file') as img:
        # The file is a valid image file.
        pass

except IOError:
    # The file is not a valid image file, or cannot be opened.
    pass
```

In this example, we use the `Image.open` method of the Pillow library to open the image file at the specified path. If the file is a valid image file, it will be parsed successfully, and we can proceed with our processing. Otherwise, an IOError exception will be raised, indicating that the file is not a valid image file or cannot be opened.

## Checking the Image Format
It is also possible to check the format of the image file before opening it. This can be useful if we want to limit the image file types that we want to process. For example, we may only want to process JPEG and PNG image files.

Here is an example code snippet that demonstrates how to do this:

``` python
from PIL import Image

def is_valid_image_file(file_path):
    """
    Returns True if the file at the specified path is a valid image file.
    """
    try:
        with Image.open(file_path) as img:
            # The file is a valid image file.
            return True

    except IOError:
        # The file is not a valid image file, or cannot be opened.
        return False

def is_supported_image_file(file_path):
    """
    Returns True if the file at the specified path is a supported image file format.
    """
    supported_formats = ('JPEG', 'PNG')
    file_format = Image.open(file_path).format
    return file_format in supported_formats

file_path = 'path/to/image_file'

if is_supported_image_file(file_path) and is_valid_image_file(file_path):
    # The file is a valid and supported image file.
    pass
```

In this example, we define two functions: `is_valid_image_file` and `is_supported_image_file`. The `is_valid_image_file` function checks whether the file at the specified path is a valid image file, using the same technique we described earlier. The `is_supported_image_file` function checks whether the file is a supported image file format (JPEG or PNG in this example).

Finally, in our main code block, we check whether the file is both a valid and supported image file before proceeding with our processing.
