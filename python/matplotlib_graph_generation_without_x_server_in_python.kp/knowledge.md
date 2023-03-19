---
title: Creating matplotlib charts without the need for a running x server
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To generate matplotlib graphs without a running X server in Python, use Matplotlib`s Agg backend, which allows you to generate plots and save them to image files without displaying them on screen.
---

**Contents**

[TOC]

## Introduction
Matplotlib is a plotting library for Python programming language and creates quality graphs for data visualization. By default, matplotlib relies on a running X server to create graphs. However, sometimes there is a requirement to generate graphs without a running X server. This can be achieved using the following methods.

## Using Agg backend for matplotlib
Matplotlib can be configured to use the Agg backend which does not require a running X server. The Agg backend is a non-interactive backend that creates bitmap images of the graphs designed for computing environments without display hardware or the ability to run an X server. This can be done by setting the backend to Agg by including the following code snippet at the beginning of the script.

```python
import matplotlib
matplotlib.use('Agg')
```

## Using a headless web browser
Another way to generate graphs without a running X server is to use a headless web browser such as PhantomJS, which can render the graphs to images. The `selenium` module can be used to control the browser and generate the graphs. The following code is an example of this method.

```python
from selenium import webdriver

# Set up the browser
options = webdriver.PhantomJS()
options.add_argument('--no-sandbox')
options.add_argument('--disable-dev-shm-usage')
options.add_argument('--ignore-certificate-errors')
options.add_argument('--disable-gpu')
options.add_argument('--headless')

# Draw the graph
browser = webdriver.PhantomJS(options=options)
browser.get('http://localhost/path/to/graph')
browser.save_screenshot('/path/to/output/image.png')
```

## Using a virtual framebuffer
A virtual framebuffer is a software implementation of a graphics display. The `xvfb` package can be used to set up a virtual framebuffer and allows for the creation of graphs through a headless environment. The following code shows an example of creating a graph using a virtual framebuffer.

```python
import matplotlib
matplotlib.use('Agg')

from pyvirtualdisplay import Display
from matplotlib import pyplot as plt

# Set up virtual X display
display = Display(visible=0, size=(1024, 768))
display.start()

# Draw the graph
plt.plot([1,2,3,4])
plt.savefig('/path/to/output/image.png')

# Close the virtual X display
display.stop()
```

## Conclusion
In this article, we have outlined three ways to generate matplotlib graphs without a running X server. Each of these methods has its advantages and drawbacks, and the choice of which to use depends on the specific requirements and constraints of the environment in which the code is being executed.
