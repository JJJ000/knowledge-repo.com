---
title: What is the process for accessing a file in order to read from and write to it?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To open a file for both reading and writing in Python, use the `r+` mode when opening the file.
---

**Contents**

[TOC]

1. **Import the `open` Function**

To open a file for both reading and writing, you must first import the `open` function from the `io` module.

```python
from io import open
```

2. **Open the File**

Once the `open` function is imported, you can use it to open the desired file.

```python
file = open('filename.txt', 'r+')
```

The first argument is the path to the file, and the second argument is the mode in which the file should be opened. The `'r+'` mode opens the file for both reading and writing.

3. **Read and Write to the File**

Once the file is opened, you can read from and write to the file.

To read from the file, you can use the `read` method.

```python
text = file.read()
```

To write to the file, you can use the `write` method.

```python
file.write('Some text')
```

4. **Close the File**

Once you are done reading and writing to the file, it is important to close the file.

```python
file.close()
```
