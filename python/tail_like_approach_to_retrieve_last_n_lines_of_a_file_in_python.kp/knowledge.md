---
title: Obtain the final n lines of a file, akin to the functionality of the tail command
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To get the last n lines of a file in Python, use the built-in function `readlines()` to read all the lines of the file, and then slice the list of lines to get the desired number of lines from the end.
---

**Contents**

[TOC]

## The Problem

Suppose we have a large text file and we want to view only the last few lines of the file. This is a common problem in programming, especially when working with log files or other text files where the most recent entries are more relevant than the earlier ones. Python provides a way to solve this problem using the `tail` function.

## Using the `tail` function in Python

Python's `tail` function is part of the built-in `collections` module. It takes two arguments: the file object and the number of lines to return. Here is an example of how to use it:

```python
from collections import deque

def tail(f, n):
    return deque(f, n)
    
with open('large_file.txt', 'r') as f:
    last_lines = tail(f, 10)
    for line in last_lines:
        print(line)
```

In this example, we first import the `deque` class from the `collections` module. This class allows us to efficiently extract the last `n` items from a sequence. We define a `tail` function that takes a file object `f` and the number of lines `n` we want to extract. We then use the `deque` constructor to create a new deque instance, passing in the file object `f` and the size `n`.

Finally, we iterate over the last `n` lines of the file and print them to the console.

## Handling Errors

There are a few things that can go wrong when using the `tail` function. For example:

- The file could be empty, in which case we don't want to return anything.
- The number of lines we want to extract could be greater than the number of lines in the file, in which case we want to return all the lines.

Here's an updated version of the `tail` function that handles these edge cases:

```python
def tail(f, n):
    try:
        f.seek(0, 2)
        file_size = f.tell()
        block_size = 1024
        block_count = -(-file_size // block_size)
        lines = []
        for i in range(1, block_count + 1):
            f.seek(-i * block_size, 2)
            data = f.read(block_size)
            lines.extend(data.splitlines())
            if len(lines) >= n:
                break
        return lines[-n:]
    except IOError:
        return []
```

In this updated version, we use a try-except block to catch any potential errors. Inside the try block, we first seek to the end of the file to get its size. We then define a block size of 1024 bytes and calculate the number of blocks needed to read the entire file.

We then iterate over each block from the end of the file, reading its data and adding any lines to our list of lines. We stop iterating once we have enough lines or we've read the entire file.

Finally, we return the last `n` lines of the file or an empty list if there was an error.

## Conclusion

In conclusion, Python's `tail` function is a handy utility for extracting the last few lines from a text file. With a little bit of error handling, it's a reliable way to view the most recent entries in a log file or other text document.
