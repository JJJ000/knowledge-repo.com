---
title: Demonstrate how to track the advancement of a Python multiprocessing pool's imap_unordered function call
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: There is no direct way to track the progress of a Python multiprocessing pool imap\_unordered call.
---

**Contents**

[TOC]

# Introduction
Python multiprocessing is a way of running multiple processes at the same time in parallel to quickly and efficiently execute various tasks. One of the most frequently used functions in multiprocessing is imap_unordered, which applies a function to every item in an iterable and returns a generator that yields the results as they become available. The advantage of using imap_unordered over map is that it does not wait for all the function calls to finish before returning the first result.

# Starting the imap_unordered call
When executing an imap_unordered call, the first step is to create an instance of the multiprocessing.Pool class with the desired number of worker processes. This can be done using the following code:

```python
import multiprocessing

def func(x):
    # This is the function to be applied using imap_unordered
    pass

if __name__ == '__main__':
    pool = multiprocessing.Pool(processes=4) # Set the number of worker processes
    results = pool.imap_unordered(func, iterable) # Start the imap_unordered call
```
Here, the variable "iterable" is the iterable object which will be passed to the function one at a time, and "func" is the function to be applied to each item. The variable "results" will hold the generator object which will yield the results as they become available.

# Monitoring progress of an imap_unordered call
To monitor the progress of an imap_unordered call, we can use the built-in "tqdm" library, which provides a progress bar for a given iterator. The library can be installed using pip with the following command:

```python
pip install tqdm
```

Once installed, the following code can be used to monitor the progress of the imap_unordered call:

```python
from tqdm import tqdm

if __name__ == '__main__':
    with multiprocessing.Pool(processes=4) as pool:
        results = list(tqdm(pool.imap_unordered(func, iterable), total=len(iterable)))
```

Here, the "tqdm" function is used to create a progress bar for the imap_unordered generator, and the "list" function is used to convert the generator to a list. The progress bar will update dynamically as each item is processed, showing the percentage of completion, the elapsed time, and an estimated time remaining.

# Handling exceptions during an imap_unordered call
When executing an imap_unordered call, it is possible for an exception to be raised during the processing of an item. To handle these exceptions, we can use the "imap_unordered" function's error_callback parameter. The error_callback function will be called with the exception object whenever an exception is raised during processing.

```python
def error_handling(e):
    # Code to handle the exception object
    pass

if __name__ == '__main__':
    with multiprocessing.Pool(processes=4) as pool:
        results = list(pool.imap_unordered(func, iterable, error_callback=error_handling))
```

Here, the "error_handling" function is used to handle any exceptions that may be raised during processing, and is passed to the imap_unordered call using the error_callback parameter. If an exception is raised during processing, the error_callback function will be called with the exception object as its argument, and the processing of the item will be stopped.
