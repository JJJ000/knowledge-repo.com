---
title: A script in Python for duplicating text to the clipboard
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use `pyperclip` module to copy text to clipboard in Python.
---

**Contents**

[TOC]

## Introduction 

In this tutorial, we will be discussing how to copy text to the clipboard using Python. The clipboard is a temporary data storage area that holds text, images, and other types of data temporarily until the user decides to paste it. Python has several ways to accomplish this task, whether it is using external libraries or using a few lines of code. 

## Using Python Built-In Clipboard Module 

Python has a built-in clipboard module that can be used to copy and paste data from the clipboard. Here is how to achieve this step by step:

1. Install the pyperclip module using pip: 

```python
!pip install pyperclip
```

2.  Import and use the `pyperclip` module. 

```python 
import pyperclip
```
3. Copy the text you want to the clipboard.

```python
text = "sample text"
pyperclip.copy(text)
```
4. You can then paste the text using Ctrl + V or right-click and select paste from the context menu. 


## Using Third-Party Clipboard Libraries

In addition to the built-in clipboard module, there are third-party libraries that can be used to access the clipboard from Python. Some of these libraries are:

1. pyperclip: A cross-platform Python module that helps to copy and paste text, supporting both "Ctrl+C" and "Ctrl+V" on Windows, Linux, and Mac.
2. clipboard: A Python module to copy and paste text to the clipboard.

Let's use `clipboard` as an example: 

1. Install the clipboard module using pip: 

```python
!pip install clipboard
```

2. Import the module.

```python
import clipboard
```
3. Copy the text you want to the clipboard.

```python
text = "sample text"
clipboard.copy(text)
```
4. You can then paste the text using Ctrl + V or right-click and select paste from the context menu. 

## Conclusion 

In conclusion, you can use either the built-in Python clipboard module or third-party libraries such as pyperclip and clipboard to copy text to the clipboard. While using the third-party libraries may give you more control over the clipboard, it's always best to use the built-in clipboard module unless you need more complex functionality that is not supported by it.
