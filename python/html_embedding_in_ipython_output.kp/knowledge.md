---
title: What are the steps to include html in the output of ipython?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `IPython.display.HTML` function to display HTML code as output in IPython.
---

**Contents**

[TOC]

## Introduction
IPython is a powerful tool that enables researchers, engineers and data scientists to code and execute Python code in a multi-language interactive environment. One of the strengths of IPython is the ability to include rich media output, including HTML. This allows users to create interactive presentations, dashboards, and other visualizations within an IPython notebook. In this tutorial, we will show you how to embed HTML into IPython output.

## Using IPython's Display module
IPython's Display module provides a simple way to render HTML code as output. To use this module, first, we must import it into our notebook.

```python
from IPython.display import display, HTML
```
Once the Display module is imported, we can use the `HTML` class to render HTML code. We do this by creating a new instance of the class containing the HTML code we want to display, and then passing that instance to the `display` function. Here is an example:

```python
html_code = "<h1>This is a heading</h1><p>This is some text</p>"
html = HTML(html_code)

display(html)
```

This will output:

<h1>This is a heading</h1><p>This is some text</p>

## Using Jupyter widgets to incorporate HTML code
Jupyter widgets allow us to create interactive graphical user interfaces within our IPython notebook. They also provide a way to incorporate HTML code into the notebook more easily. 

```python
import ipywidgets as widgets
from IPython.display import display

button = widgets.Button(description="Click Me!")
display(button)

def on_button_clicked(b):
    print("Button clicked.")

button.on_click(on_button_clicked)
```

This will create a button element in the notebook, and when clicked, it will trigger a Python function that prints to the notebook output.

## Conclusion
In this tutorial, we demonstrated two ways to embed HTML code into IPython output. Using IPython's Display module is a simple approach that is useful when we need to display static HTML. Using Jupyter widgets provides a more dynamic approach that enables us to create interactive user interfaces.
