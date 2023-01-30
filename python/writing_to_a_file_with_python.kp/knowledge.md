---
title: Creating a text file with a list of items in python, each item on a separate line
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `write()` method of a file object to write a string containing a list with newlines to a file.
---

**Contents**

[TOC]

### Section 1: Opening the File

We need to open the file in write mode so that we can write to it. We can do this using the `open()` function:

```python
f = open("my_list_file.txt", "w")
```

### Section 2: Writing the List

We can write the list to the file using a `for` loop:

```python
my_list = ["apples", "oranges", "bananas"]
for item in my_list:
    f.write(item + "\n")
```

This will write each item in the list to the file, followed by a newline character.

### Section 3: Closing the File

Finally, we need to close the file when we are done writing to it:

```python
f.close()
```

### Section 4: Final Code

Putting it all together, our final code looks like this:

```python
f = open("my_list_file.txt", "w")
my_list = ["apples", "oranges", "bananas"]
for item in my_list:
    f.write(item + "\n")
f.close()
```
