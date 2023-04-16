---
title: Iterating through each byte of a binary file while reading it
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To read each byte in a binary file in Python, you can use a for loop to iterate over the file object`s read() method.
---

**Contents**

[TOC]

### Section 1: Opening the File

In order to open a binary file in Python, we must use the `open()` method. The `open()` method requires two parameters: the file name and the mode. To open a binary file, we must specify the mode as `'rb'` for read binary. 

```python
f = open("myfile.bin", "rb")
```

### Section 2: Reading the File

Once the file has been opened, we can read the contents of the file by using the `read()` method. This method will return the contents of the file as a byte object.

```python
contents = f.read()
```

### Section 3: Looping Over Each Byte

We can now loop over each byte in the file by using a `for` loop. The `for` loop will iterate over each byte in the `contents` object returned by the `read()` method.

```python
for byte in contents:
  # Do something with the byte
```

### Section 4: Closing the File

When we are finished looping over the file, we must close the file using the `close()` method.

```python
f.close()
```
