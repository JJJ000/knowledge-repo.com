---
title: What is the dimensions of an image when using pil?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the size attribute of the Image object.
---

**Contents**

[TOC]

# 1. Import Libraries

First, import the necessary libraries:

```python
from PIL import Image
```

# 2. Open Image

Next, open the image using the `Image.open()` function:

```python
im = Image.open('my_image.jpg')
```

# 3. Get Size

Finally, use the `.size` attribute to get the size of the image:

```python
width, height = im.size
```

# 4. Print Size

Optionally, you can print the size of the image:

```python
print('The size of the image is {} x {}'.format(width, height))
```
