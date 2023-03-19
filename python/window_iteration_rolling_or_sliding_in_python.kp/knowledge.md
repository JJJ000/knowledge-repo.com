---
title: Could you iterate using a rolling or sliding window?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: A sliding window iterator in Python can be implemented using a generator function that yields successive n-sized chunks of an input iterable.
---

**Contents**

[TOC]

Introduction
------------

In Python, an iterator is a mechanism to traverse a collection of elements one by one. When it comes to working with large data sets, it is often necessary to use a window iterator to process a subset of elements at a time. There are two types of window iterators - rolling and sliding window iterators. In this article, we will discuss both types of window iterators in Python.

Rolling Window Iterator
------------------------

A rolling window iterator processes a fixed-size window of elements at a time. It moves the window forward one element at a time and processes the new window. This type of iterator is useful when we need to work with fixed-size subsets of large data sets. We can implement a rolling window iterator in Python using the `itertools` module.

Here's an example of a rolling window iterator in Python:

```python
from itertools import tee

def rolling_window(iterable, size):
    iters = tee(iterable, size)
    for i, it in enumerate(iters):
        for _ in range(i):
            next(it, None)
    yield from zip(*iters)
```

In the above example, we first create `size` number of copies of the iterable using the `tee` function from the `itertools` module. We then move each copy forward `i` steps so that the `i`th element becomes the first element of the window. Finally, we use the `zip` function to group the elements of each copy into a single window.

Sliding Window Iterator
-----------------------

A sliding window iterator, unlike a rolling window iterator, moves the window forward by a fixed amount of steps instead of one element at a time. This type of iterator is useful when we need to work with overlapping subsets of large data sets. We can implement a sliding window iterator in Python using the `itertools` module.

Here's an example of a sliding window iterator in Python:

```python
from itertools import islice

def sliding_window(iterable, size, step=1):
    it = iter(iterable)
    results = tuple(islice(it, size))
    if len(results) == size:
        yield results
    while True:
        results = results[step:] + tuple(islice(it, step))
        if len(results) == size:
            yield results
        else:
            break
```

In the above example, we first create a tuple of the first `size` elements of the iterable using the `islice` function from the `itertools` module. We then yield this tuple as the first window. We then use a while loop to move the window forward `step` steps at a time, stopping when we are unable to create another window of `size` elements. Finally, we yield the last window (if any).

Conclusion
----------

In Python, we can use both rolling and sliding window iterators to process large data sets. Rolling iterators are useful when we need to work with non-overlapping fixed-size subsets of elements, while sliding iterators are useful when we need to work with overlapping subsets of elements. We can implement both types of iterators using the `itertools` module in Python.
