---
title: Creating a png image using matplotlib when the display variable is not set
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can save the plot as a PNG file using the plt.savefig() function.
---

**Contents**

[TOC]

**Solution 1 - Use Agg Backend**

Matplotlib provides a backend called Agg, which is a non-interactive backend. This backend will not open a window, but it will generate a PNG file. To use this backend, you can set it in the matplotlib configuration file:

```
import matplotlib
matplotlib.use('Agg')
```

**Solution 2 - Use plt.savefig()**

Another way to generate a PNG file with matplotlib when the DISPLAY is undefined is to use the `plt.savefig()` function. This function will save the current figure to a file. The file format is determined by the file extension you specify. To save a PNG file, you can use the following code:

```
plt.savefig('filename.png')
```

**Solution 3 - Use plt.show()**

Another solution is to use the `plt.show()` function. This function will open a window and display the figure, but it will also save the figure to a file. To save the figure to a file, you can specify the `filename` parameter:

```
plt.show(filename='filename.png')
```

**Solution 4 - Use a Headless Display**

If you are running your Python script on a headless server, you can use a headless display such as Xvfb to generate a PNG file. Xvfb is a virtual framebuffer that can be used to generate a display for matplotlib. To use Xvfb, you need to install it on your system and then set the DISPLAY environment variable to point to the Xvfb display. You can then use the `plt.show()` or `plt.savefig()` functions to generate a PNG file.
