---
title: I am getting an error that says "modulenotfounderror no module named 'cv2' when using opencv"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You need to install the OpenCV package for Python before you can use it.
---

**Contents**

[TOC]

### Install OpenCV

OpenCV can be installed by downloading the appropriate binary from the [OpenCV website](https://opencv.org/releases/). Once downloaded, the package should be extracted and installed according to the instructions provided.

### Install cv2

Once OpenCV is installed, the cv2 module can be installed by running the following command in the terminal:

`pip install opencv-python`

This will install the cv2 module, which will allow you to use OpenCV in Python.

### Verify Installation

Once cv2 is installed, you can verify the installation by running the following command in the terminal:

`python -c "import cv2; print(cv2.__version__)"`

This should print out the version of cv2 that is installed.

### Troubleshooting

If you are still having trouble installing cv2, you can try uninstalling and reinstalling OpenCV and cv2, or you can try using a different version of OpenCV.
