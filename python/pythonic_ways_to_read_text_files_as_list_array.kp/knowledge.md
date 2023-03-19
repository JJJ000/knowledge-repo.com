---
title: How can Python be used to load a text file into an array or a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `readlines()` method to read the contents of the text file into a list.
---

**Contents**

[TOC]

### Section 1: Opening the File

The first step in reading a text file into a list or an array with Python is to open the file. To do this, we can use the built-in function in Python called `open()`. The `open()` function takes two arguments: the name of the file and the mode. The mode specifies whether we are reading, writing, or appending to the file. In this case, we want to read the file, so we will use the mode `'r'`.

```python
file = open('filename.txt', 'r')
```

### Section 2: Reading the File Line by Line

Now that we have opened the file, we can read its contents line by line. In Python, we can use a `for` loop to iterate over the lines of the file. Each line in the file is a string, and we can strip any whitespace characters using the `strip()` function. We can then append each line to a list or an array.

```python
lines = []
for line in file:
    lines.append(line.strip())
```

Alternatively, we can use the `readlines()` function of the file object to read all the lines of the file at once and return them as a list.

```python
lines = file.readlines()
```

### Section 3: Closing the File

After we have finished reading the file, it is important to close it using the `close()` function. This ensures that any resources allocated by the operating system to the file are released.

```python
file.close()
```

### Section 4: Putting it all Together

To summarize, to read a text file into a list or an array with Python, we need to perform the following steps:

1. Open the file using the `open()` function with mode `'r'`.
2. Read the file line by line using a `for` loop or the `readlines()` function.
3. Append each line to a list or an array.
4. Close the file using the `close()` function.

Here is an example code snippet that puts it all together:

```python
filename = 'example.txt'
with open(filename, 'r') as file:
    lines = file.readlines()

print(lines)
```
