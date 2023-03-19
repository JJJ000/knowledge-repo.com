---
title: What is the method to import a file as a list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To read a file into a list in Python, use the `readlines()` method.
---

**Contents**

[TOC]

## Opening and reading the file

To read a file into a list in Python, we need to first open the file and read its contents. We can do this with the built-in function `open()`:

```python
file = open('filename.txt')
```

This will open the file in read mode by default. To read the contents of the file, we can use the `readlines()` method:

```python
lines = file.readlines()
```

This will read all the lines in the file and return them as a list of strings, where each string represents one line in the file. 

## Closing the file

Once we have read the file, it's important to close it using the `close()` method:

```python
file.close()
```

This will free up any system resources that were being used by the file and prevent any potential issues that could arise from leaving the file open for too long.

## Complete code

Putting it all together, here's how we can read a file into a list in Python:

```python
file = open('filename.txt')
lines = file.readlines()
file.close()

print(lines)
```

This will open the file `'filename.txt'`, read its contents into a list of lines stored in the variable `lines`, close the file, and then print the list of lines to the console.
