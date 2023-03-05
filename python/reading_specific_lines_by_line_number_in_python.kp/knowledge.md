---
title: Can you provide a method for accessing particular lines in a file based on line numbers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the readline() method in a loop, keeping track of the line number and stopping when the desired line is reached.
---

**Contents**

[TOC]

## Introduction
Sometimes, there may be a need to read specific lines from a file by line number. In Python, there are several ways to do this. In this article, we'll cover a few popular approaches.

## Using the `linecache` module
The `linecache` module provides a simple way to access specific lines of a file by number. 

```python
import linecache

# get the 3rd line of file.txt
line = linecache.getline('file.txt', 3)

print(line)
``` 

The `getline` function takes two parameters: the file name and the line number. It returns the specified line as a string.

## Using `enumerate` and a loop
Another approach is to use a loop and `enumerate` to read the file line by line and then only keep the lines with the specified line numbers.

```python
# read lines 3, 5, and 7 from file.txt
line_numbers = [3, 5, 7]

with open('file.txt') as file:
    for number, line in enumerate(file, 1):
        if number in line_numbers:
            print(line.strip())
```

We first create a list of the line numbers we want to read. We then open the file using a `with` statement and loop over the lines using `enumerate`. We use the `strip` method to remove any trailing whitespace from the lines. We only print the lines where the line number is in our list of line numbers.

## Using `itertools.islice`
The `islice` function from the `itertools` module can also be used to get specific lines from a file.

```python
import itertools

# read lines 3, 4, and 5 from file.txt
line_numbers = [3, 4, 5]

with open('file.txt') as file:
    for line in itertools.islice(file, 2, 5):
        print(line.strip())
```

In this example, we pass a `start` and `stop` parameter to `islice` to specify the range of lines we want to read. We subtract `1` from each line number to get the correct indexes (since lists are 0-indexed).

## Conclusion
These are just a few examples of how to read specific lines from a file in Python. Depending on the situation, one approach may be more suitable than others.
