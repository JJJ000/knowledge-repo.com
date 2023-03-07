---
title: Reword 'collapse cell in jupyter notebook'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To collapse a cell in Jupyter Notebook, simply click on the blue line on the left side of the cell.
---

**Contents**

[TOC]

1. Introduction
In a Jupyter notebook, cells can contain various forms of input such as text, code, and output. When working on a long notebook, it may be helpful to collapse certain cells to declutter the interface and improve readability. In this article, we will explore several ways to collapse cells in a Jupyter notebook using Python.

2. Collapsing Cells using Code
One way to collapse cells in a Jupyter notebook is to use code to hide or show the contents of a cell when a certain button or event is triggered. The `IPython.display` module provides the functions `display()` and `HTML()` which can be used to add HTML elements to the notebook. Here is an example code block that demonstrates how to create a collapsible section in a notebook:

```python
from IPython.display import display, HTML

display(HTML("""
    <details>
        <summary>Click to expand/collapse</summary>
        Contents of the collapsed section go here ...
    </details>
"""))
```

In this code block, we create an HTML `details` element that contains a `summary` element as well as the contents of the collapsed section. The `display()` function is used to add the HTML element to the notebook.
 
3. Collapsing Cells using nbextensions
Another way to collapse cells in a Jupyter notebook is to use nbextensions – a collection of community-contributed unofficial extensions. Nbextensions can add new features and functionality to a Jupyter notebook and there are many extensions available that enable cell collapsing. To use an nbextension, you need to install and enable it first. Here are the steps to follow to install and enable an nbextension that adds collapsible sections to Jupyter notebooks:

- Install the `jupyter_contrib_nbextensions` package using pip:

```python
pip install jupyter_contrib_nbextensions
```

- Install the nbextension package by running this command:

```python
jupyter contrib nbextension install --user
```

- Enable the collapsible headings nbextension:

```python
jupyter nbextension enable collapsible_headings/main
```

After enabling the nbextension, you will find new icons in the toolbar that allow you to collapse or expand all the headings in a notebook.

4. Collapsing Cells using Markdown
Finally, you can collapse cells in a Jupyter notebook using Markdown by adding collapsible sections to a Markdown cell. This method involves using Markdown syntax to create collapsible sections manually. Here is an example Markdown cell that demonstrates how to create a collapsible section:

```
<details>
  <summary>Click to expand/collapse</summary>

  Your content goes here...

</details>
```

In this Markdown cell, the `details` element is used to create a collapsible section. The `summary` element is used to define the title of the section and the contents of the section go between the opening `<details>` and closing `</details>` tags.

Conclusion
In conclusion, there are several ways to collapse cells in a Jupyter notebook using Python. We explored three methods: using code to create collapsible sections, enabling an nbextension that adds collapsible headings, and using Markdown syntax to create collapsible sections manually. These methods can help improve the readability and organization of your Jupyter notebook.
