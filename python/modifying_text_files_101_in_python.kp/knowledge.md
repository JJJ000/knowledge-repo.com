---
title: What are the steps to make changes to a text file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Open the file in write mode and use the write() function to modify the contents of the file.
---

**Contents**

[TOC]

## Reading the File

The first step in modifying a text file in Python is to read its contents. We can read a text file using the `open()` function that takes two arguments - the name of the file and the mode in which we want to open it. In our case, the mode should be 'r' for reading.

```python
with open('myfile.txt', 'r') as file:
    contents = file.read()
```

## Modifying the File

Once we have read the contents of the file, we can modify it using string manipulation methods in Python such as replace, split and join.

For example, if we want to replace a particular string in the file with another string, we can use the `replace()` method. This method takes two arguments - the string to be replaced and the replacement string.

```python
new_contents = contents.replace('old string', 'new string')
```

Similarly, we can split the contents of the file into a list of lines using the `splitlines()` method and modify the lines as required before joining them back into a single string using the `join()` method.

```python
lines = contents.splitlines()
modified_lines = [line.upper() for line in lines]
new_contents = '\n'.join(modified_lines)
```

## Writing the File

Once we have modified the contents of the file, we can write the modified contents back to the file using the `open()` function in write mode ('w').

```python
with open('myfile.txt', 'w') as file:
    file.write(new_contents)
```

It is important to note that opening a file in write mode will overwrite the existing contents of the file. If we want to append new contents to the file, we should use the append mode ('a').

```python
with open('myfile.txt', 'a') as file:
    file.write('\nNew line to be appended.')
```
