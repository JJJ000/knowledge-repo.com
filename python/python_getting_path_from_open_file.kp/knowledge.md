---
title: Retrieve the path of an opened file in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `name` attribute on a file object to get the path of the file it opened in Python.
---

**Contents**

[TOC]

### Introduction

In Python, we can use the `tkinter.filedialog` module to open a file dialogue box and select a file. Once we select a file, we can use the `os.path` module to extract the path to the file. In this tutorial, we will see how to get the path from an open file in Python. The tutorial will be split into three sections.

1. Opening file dialogue box
2. Extracting path from the selected file
3. Putting it all together

### Opening file dialogue box

To open the file dialogue box, we will use the `tkinter.filedialog` module. Below is the code for the same.

```python
import tkinter as tk
from tkinter import filedialog

root = tk.Tk()
root.withdraw()

file_path = filedialog.askopenfilename()
```

The `root.withdraw()` line hides the blank window that would normally appear with the file dialogue box. The `askopenfilename()` function displays the file dialogue box and returns the selected file's path.

### Extracting path from the selected file

Now that we have the file path, we can extract the path from the file name using the `os.path.dirname()` function. Below is the code for the same.

```python
import os

file_directory = os.path.dirname(file_path)
```

The `os.path.dirname()` function returns the directory name of `file_path`.

### Putting it all together

Finally, let us put everything together in a program.

```python
import tkinter as tk
from tkinter import filedialog
import os

root = tk.Tk()
root.withdraw()

file_path = filedialog.askopenfilename()
file_directory = os.path.dirname(file_path)

print(file_directory) # Print path to the selected file
```

This program will open the file dialogue box, let us select a file, extract the path, and print it to the console.

### Conclusion

In this tutorial, we saw how to get the path from an open file in Python. We used the `tkinter.filedialog` module to open the file dialogue box and the `os.path` module to extract the path from the selected file.
