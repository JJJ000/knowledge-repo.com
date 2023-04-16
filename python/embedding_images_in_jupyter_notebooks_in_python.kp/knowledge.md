---
title: What is the process for adding an image or picture to a jupyter notebook from a local computer or from the internet?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To embed an image or picture in a Jupyter Notebook, use the `IPython.display.Image` function to display the image from either a local machine or a web resource.
---

**Contents**

[TOC]

#### Embedding from a Local Machine

1. Firstly, you need to upload the image file to the Jupyter Notebook environment. You can do this by clicking the upload button in the top right corner of the Jupyter Notebook page.

2. Once the image is uploaded, you can embed it into the notebook by using the `<img>` HTML tag. For example, if the file name of your image is `my_image.jpg`, you can embed it using the following code:

```
<img src="my_image.jpg" alt="My Image" />
```

#### Embedding from a Web Resource

1. To embed an image from a web resource, you need to get the URL of the image. You can do this by right-clicking on the image and selecting “Copy Image Address”.

2. Once you have the URL, you can embed the image into the notebook by using the `<img>` HTML tag. For example, if the URL of your image is `https://example.com/my_image.jpg`, you can embed it using the following code:

```
<img src="https://example.com/my_image.jpg" alt="My Image" />
```
