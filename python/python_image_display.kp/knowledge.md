---
title: Show a picture using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To display an image in Python, you can use the PIL (Python Imaging Library) module or the matplotlib library.
---

**Contents**

[TOC]

## Installing Pillow Library

To display an image with Python, we need to use the Pillow library. To install it, we can use the following command:

```python
pip install Pillow
```


## Loading an Image

After installing Pillow, we can load an image using the `Image` module. Here's an example:

```python
from PIL import Image

image = Image.open('image.jpg')
```

Note that the `open` function takes the path of the image file as an argument.


## Displaying an Image

To display the loaded image, we can use the `show` method of the `Image` module. Here's how:

```python
image.show()
```

This will open the image file with the default image viewer of your operating system.


## Putting it All Together

Here's an example code that loads and displays an image:

```python
from PIL import Image

image = Image.open('image.jpg')
image.show()
```

Make sure to replace `image.jpg` with the path of your own image file.
