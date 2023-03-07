---
title: What is the method for reading the initial n lines of a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `readlines()` method with argument `N` on the file object to read the first N lines of the file into a list.
---

**Contents**

[TOC]

## Introduction

Python provides various ways to read and manipulates files. In this tutorial, we will look at how to read the first N lines of a file in Python.

## Using the readlines() method

Python provides a built-in method called `readlines()` for reading lines from a file. We can use this method to read the first N lines of a file.

We can pass the number of lines we want to read as an argument to the `readlines()` method. The method will return a list of strings, where each string represents a line from the file.

Here's an example code snippet:

```python
with open('file.txt', 'r') as f:
    lines = f.readlines(5)

print(lines)
```

In the above code, we are opening a file called `file.txt` in read mode using the `with` statement. We are then calling the `readlines()` method by passing 5 as an argument, which will read the first 5 lines of the file. The `readlines()` method returns a list of strings, which we are storing in the `lines` variable. Finally, we are printing the `lines` variable.

## Using a for loop

Another approach to read the first N lines of a file is to use a for loop. We can use a for line in file operation to loop through the file and break after reading the first N lines.

Here's an example code snippet:

```python
with open('file.txt', 'r') as f:
    for line in f:
        print(line.strip())
        n -= 1

        if n == 0:
            break
```

In the above code, we are opening a file called `file.txt` in read mode using the `with` statement. We are then using a for loop to loop through the file line by line. We are printing each line and decrementing the value of N by 1. We are also checking if N has reached 0, in which case we break out of the for loop.

## Using itertools

Python provides a module called itertools that contains various functions for working with iterable objects. The `islice` function in itertools can be used to read the first N lines of a file.

Here's an example code snippet:

```python
from itertools import islice

with open('file.txt', 'r') as f:
    lines = list(islice(f, 5))

print(lines)
```

In the above code, we are importing the `islice` function from the `itertools` module. We are then opening a file called `file.txt` in read mode using the `with` statement. We are then using the `islice` function to read the first 5 lines of the file. We are storing the lines in a list using the `list()` function, which we are storing in the `lines` variable. Finally, we are printing the `lines` variable.
