---
title: What is the proper way to read a file one line at a time using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use a for loop to iterate through each line in the file.
---

**Contents**

[TOC]

### Opening the file

To read a file line-by-line in Python, the first step is to open the file using the `open()` function. The `open()` function takes two arguments: the filename and mode. The mode specifies the way in which the file is opened. To read the file line-by-line, the mode should be set to `'r'`, which means read mode.

```python
file = open('filename.txt', 'r')
```

### Reading the file line-by-line

Once the file has been opened, you can read the file line-by-line using a `for` loop. The `for` loop iterates through each line of the file, and the `readline()` function is used to read each line.

```python
for line in file:
    print(line)
```

Alternatively, you can use the `readlines()` function, which reads the entire file into a list of lines. Then you can loop through the list to iterate over the lines.

```python
lines = file.readlines()

for line in lines:
    print(line)
```

### Closing the file

After you have finished reading the file, you should close it using the `close()` method, as it frees up system resources.

```python
file.close()
```

### Using the `with` statement

It is considered good practice to use the `with` statement when working with files in Python. The `with` statement automatically closes the file for you when you exit the block.

```python
with open('filename.txt', 'r') as file:
    for line in file:
        print(line)
```

In this case, you don't need to explicitly close the file using the `close()` method as the `with` statement takes care of it for you.
