---
title: What is the method for writing bytes to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To write bytes to a file in Python, open the file in binary mode and use the write() method to write the bytes.
---

**Contents**

[TOC]

Section 1: Opening a file
To write bytes to a file in Python, you first need to open the file. You can do this using the `open()` function, which takes two arguments:

- The first argument is the file name, including the path if the file is not in the current working directory.
- The second argument is the mode in which the file should be opened. In this case, you want to open the file in binary mode, so you should use the `'wb'` mode.

Example:

```python
filename = 'example.bin'
with open(filename, 'wb') as f:
    # File operations go here
```

Section 2: Writing bytes to a file
Once you have a file object, you can write bytes to it using the `write()` method. This method takes a bytes object as an argument, which you can create using the `bytes()` or `bytearray()` built-in functions.

Example:

```python
filename = 'example.bin'
data = bytes([0x41, 0x42, 0x43])
with open(filename, 'wb') as f:
    f.write(data)
```

In this example, the `bytes()` function is used to create a bytes object containing the hexadecimal values of the ASCII characters 'A', 'B', and 'C'. This bytes object is then passed to the `write()` method of the file object, which writes the bytes to the file.

Section 3: Writing multiple bytes to a file
If you want to write more than one byte to a file, you can create a bytes object containing multiple bytes and pass it to the `write()` method.

Example:

```python
filename = 'example.bin'
data = bytes([0x41, 0x42, 0x43, 0x44, 0x45])
with open(filename, 'wb') as f:
    f.write(data)
```

In this example, the `bytes()` function is used to create a bytes object containing the hexadecimal values of the ASCII characters 'A', 'B', 'C', 'D', and 'E'. This bytes object is then passed to the `write()` method of the file object, which writes all five bytes to the file.

Section 4: Closing the file
After you have finished writing bytes to the file, you should close the file object using the `close()` method. This ensures that any cached data is written to the file and that the file is released for other processes to access.

Example:

```python
filename = 'example.bin'
data = bytes([0x41, 0x42, 0x43])
with open(filename, 'wb') as f:
    f.write(data)
    f.close()
```

In this example, the `close()` method is called on the file object after the bytes have been written to the file.
