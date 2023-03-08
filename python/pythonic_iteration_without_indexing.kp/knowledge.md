---
title: What is the way in Python to perform an action n number of times without using an index variable?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the range() function and a for loop, iterating over the range object without assigning the index to a variable, for example `for \_ in range(N)`.
---

**Contents**

[TOC]

# Introduction 

Sometimes we need to repeat some operation or function call in Python N times without using an index variable. In such cases, there are several Pythonic ways to achieve this.

# Using range with for loop

One way to do this is to use the built-in `range` function with a `for` loop. The `range` function creates a sequence of numbers from 0 to N-1, which can be looped over using the `for` loop. We don't need to use an index variable in this approach.

```python
N = 5
for _ in range(N):
    # operation or function call
    print("Hello, world!")
```

In the above code, we are repeating the operation of printing "Hello, world!" five times without using an index variable.

# Using itertools.repeat with map

Another way to perform an operation N times is to use the `itertools.repeat` function with the `map` function. The `itertools.repeat` function creates an iterator that repeats the same value infinitely or a specified number of times. We can use this iterator with the `map` function to perform an operation N times without using an index variable.

```python
import itertools

N = 5
map(lambda _: operation(), itertools.repeat(None, N))
```

In the above code, `itertools.repeat(None, N)` creates an iterator that repeats `None` N times. We are passing this iterator along with the `operation` function to the `map` function. The `map` function applies `operation` to each element of the iterator, which results in performing the operation N times.

# Using list comprehension

Another Pythonic way to perform an operation N times is to use a list comprehension. We can use `_` as a placeholder variable in the list comprehension to signify that we don't need to use the variable.

```python
N = 5
[operation() for _ in range(N)]
```

In the above code, `_` is used as a placeholder variable in the list comprehension. The `operation()` function is being called N times, which results in performing the operation N times.

# Conclusion

In this article, we have discussed three Pythonic ways to perform an operation or function call N times without using an index variable. We can choose from any of these approaches based on our requirements and coding style.
