---
title: What is the method to launch the interactive matplotlib window within ipython notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Add the magic command `%matplotlib inline` at the beginning of the notebook.
---

**Contents**

[TOC]

Section 1: Introduction to Matplotlib and IPython Notebook

Matplotlib is a plotting and data visualization library in Python that provides a variety of 2D and 3D plotting options. The IPython notebook is an interactive computing environment that enables researchers, data analysts, and scientists to create and document analysis workflows in a single document.

Section 2: Using matplotlib inline magic command

One way to use Matplotlib and get inline charts in IPython notebook is to use the matplotlib inline magic command. This command instructs IPython to show the plot inside the notebook rather than in a separate window. Here is an example of how to use the inline magic command.

```
%matplotlib inline
```
Note: The magic command needs to be run before importing matplotlib in the notebook.

Section 3: Opening the interactive matplotlib window in IPython Notebook

If you need to open the interactive matplotlib window in IPython notebook, you should use the interactive backend. You can activate it using the `%matplotlib` command with the `inline` argument.

```python
%matplotlib inline
import matplotlib.pyplot as plt

# Set the interactive backend
%matplotlib inline
%matplotlib notebook 

# Create a plot
fig, ax = plt.subplots()
ax.plot([1, 2, 3], [4, 5, 6])

# Show the plot
plt.show()
```

Section 4: Conclusion

In conclusion, there are different ways to use Matplotlib in IPython notebook. The most common method is to use the inline magic command, which displays the plot inside the notebook. However, if you need to open the interactive matplotlib window, you should use the `%matplotlib` command with the `notebook` argument to activate the interactive backend.
