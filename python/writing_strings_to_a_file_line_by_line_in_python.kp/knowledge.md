---
title: Adding a new line of text to a file each time something is written
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the built-in `writelines()` function to write a list of strings to a file, with each string on a new line.
---

**Contents**

[TOC]

## 1. Opening the File

The first step is to open the file in write mode.

```python
f = open("filename.txt", "w")
```

## 2. Writing to the File

To write a string to the file, use the `write()` method.

```python
f.write("This is the string to be written")
```

## 3. Adding a New Line

To add a new line after the string, add a `\n` character.

```python
f.write("This is the string to be written\n")
```

## 4. Closing the File

Finally, close the file to save the changes.

```python
f.close()
```
