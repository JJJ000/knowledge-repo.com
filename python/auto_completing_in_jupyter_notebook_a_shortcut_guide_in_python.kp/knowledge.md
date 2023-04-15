---
title: What is the alternative way of enabling autocomplete in jupyter notebook without utilizing the tab key?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To get autocomplete in Jupyter Notebook without using tab in Python, press Shift + Tab after typing the object, method or function name.
---

**Contents**

[TOC]

### Section 1: Introduction

Jupyter Notebook is a web-based interactive environment used for data science, numerical simulation, and machine learning. It allows users to conduct data analysis in code blocks organized in a notebook format. One of the essential features of Jupyter Notebook is the autocomplete function, which makes coding faster and more efficient. Autocomplete in Jupyter Notebook can be enabled using Tab, but some users prefer to use other methods.

### Section 2: Enabling Autocomplete in Jupyter Notebook

Jupyter Notebook can be configured to use autocomplete without using Tab. Here's how:

Step 1: Open the Jupyter Notebook command prompt.
Step 2: Type `jupyter nbextension enable --py widgetsnbextension` and press Enter.
Step 3: Restart the Jupyter Notebook kernel by clicking "Kernel" and selecting "Restart".

### Section 3: Using Autocomplete in Jupyter Notebook

Once autocomplete is enabled, you can use it in Jupyter Notebook without using Tab. Here's how:

Step 1: Import the `IPython` module by typing `import IPython` in a code cell and pressing Shift+Enter.
Step 2: Type a variable name followed by a period (`.`) to see the list of methods available for that variable.
Step 3: Press the Tab key to see the autocompletion suggestions.

### Section 4: Conclusion

Enabling and using autocomplete in Jupyter Notebook is a quick and easy way to speed up your coding workflow. By following the steps outlined above, you can enable autocomplete without using Tab and use it to quickly find the methods and functions that you need to complete your analysis or simulation.
