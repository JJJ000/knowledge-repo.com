---
title: What is the procedure for showing complete output in jupyter, instead of just the final outcome?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Add a semicolon (;) at the end of the line of code you want to display the full output for in Jupyter.
---

**Contents**

[TOC]

## Introduction

When working with Jupyter notebooks, it is common to run a code cell and then only see the last output displayed. However, sometimes it is useful to see the full output of a cell, including all of the intermediate outputs. This can be done by configuring the notebook settings and modifying the code to display all of the output.

## Displaying All Output in a Cell

To display all output in a cell, you can use the `display()` function from the `IPython.display` module. This will allow you to show multiple outputs in a single cell, such as printing a variable and then displaying a plot.

```python
from IPython.display import display

var = 10
display(var)
```

This will display the value of `var` in the output of the cell.

## Changing Notebook Settings

By default, Jupyter notebooks are set to only display the last output of a cell. However, you can change this setting to display all of the outputs. To do this, you need to modify the `max_rows` and `max_columns` settings in the `pandas` module. These settings determine how many rows and columns are displayed in a table or other output.

```python
import pandas as pd

pd.set_option('display.max_rows', None)
pd.set_option('display.max_columns', None)
```

With these settings, all rows and columns of a table will be displayed, instead of just a subset. This can be useful when working with large datasets or tables.

## Using Widgets to Control Output

Jupyter notebooks also have built-in widgets that can be used to control how output is displayed. For example, you can use a button widget to toggle between displaying and hiding certain outputs. To do this, you need to use the `Output` widget from the `ipywidgets` module.

```python
import ipywidgets as widgets
from IPython.display import display, clear_output

output = widgets.Output()
display(output)

button = widgets.Button(description="Display Output")
output_text = widgets.Text("This output will be hidden until the button is pressed")

def on_button_click(b):
    with output:
        clear_output()
        display(output_text)

button.on_click(on_button_click)
display(button)
```

In this example, the `output_text` widget is hidden until the `button` widget is pressed. When the button is pressed, the `output_text` widget is displayed using the `Output` widget.

## Conclusion

In summary, there are several ways to display full output in Jupyter notebooks, including using the `display()` function, changing notebook settings, and using widgets to control output. By using these techniques, you can better understand the results of your code and gain more insight into your data.
