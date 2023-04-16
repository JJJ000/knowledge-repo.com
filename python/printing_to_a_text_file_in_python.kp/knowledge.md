---
title: Write a string to a text document
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the open() function with the `w` mode to open a text file and the write() function to write a string to the file.
---

**Contents**

[TOC]

### Section 1: Opening the File

In order to write a string to a text file, we must first open the file. This is done using the `open()` function.

```python
f = open("filename.txt", "w")
```

The first argument is the name of the file you want to open and the second argument is the mode in which you want to open it. In this case, the "w" indicates that we want to open the file in write mode.

### Section 2: Writing to the File

Once the file has been opened, we can use the `write()` function to write our string to the file.

```python
f.write("This is my string")
```

The `write()` function takes a string as an argument and writes it to the file.

### Section 3: Closing the File

Once we are done writing to the file, we must close it. This is done using the `close()` function.

```python
f.close()
```

This will ensure that all the data is written to the file and that the file is properly closed.

### Section 4: Reading the File

Once the file has been written to and closed, we can use the `open()` function to open the file in read mode.

```python
f = open("filename.txt", "r")
```

The "r" indicates that we want to open the file in read mode. We can then use the `read()` function to read the contents of the file.

```python
contents = f.read()
```

The `read()` function reads the entire contents of the file and returns it as a string. We can then print the contents of the file.

```python
print(contents)
```

This will print the contents of the file, which should include the string we wrote earlier.
