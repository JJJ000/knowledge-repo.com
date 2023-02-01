---
title: What is the process for resizing an image with pil while preserving its aspect ratio?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the thumbnail() method of the Image module to resize an image while maintaining its aspect ratio.
---

**Contents**

[TOC]

# Section 1: Import the Image

Before we can begin resizing the image, we need to import it using the Pillow (PIL) library. We can do this using the following code:

```python
from PIL import Image
img = Image.open("path/to/image.jpg")
```

# Section 2: Calculate the Aspect Ratio

Next, we need to calculate the aspect ratio of the image. This is simply the ratio of the width to the height of the image. We can calculate this using the following code:

```python
width, height = img.size
aspect_ratio = width / height
```

# Section 3: Resize the Image

Now that we have the aspect ratio, we can resize the image while preserving the aspect ratio. We can do this using the `resize()` method of the Pillow library. The `resize()` method takes two parameters: the new width and the new height. To keep the aspect ratio, we can scale the width and height by the same factor.

For example, if we want to resize the image to half of its original size, we can use the following code:

```python
new_width = width / 2
new_height = height / 2
img = img.resize((int(new_width), int(new_height)))
```

# Section 4: Save the Resized Image

Finally, we need to save the resized image. We can do this using the `save()` method of the Pillow library.

```python
img.save("path/to/resized_image.jpg")
```
