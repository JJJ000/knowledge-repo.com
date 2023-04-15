---
title: Iterating over the index in 'for' loops
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: In a 'for' loop, the index of the current item can be accessed using the built-in 'enumerate' function.
---

**Contents**

[TOC]

### Overview

In Python, the index of a sequence (such as a list, tuple, or string) can be accessed in a for loop. This allows the programmer to iterate over the sequence and access each element in the sequence, as well as its corresponding index. 

### Syntax

The syntax for accessing the index in a for loop is as follows:

```python
for index, item in enumerate(sequence):
    # Do something with index and item
```

### Example

Here is an example of accessing the index in a for loop:

```python
my_list = ["a", "b", "c"]

for index, item in enumerate(my_list):
    print("The index of", item, "is", index)
```

This will print the following output:

```python
The index of a is 0
The index of b is 1
The index of c is 2
```

### Conclusion

In conclusion, accessing the index in a for loop in Python is a useful tool for iterating over a sequence and accessing each element in the sequence along with its corresponding index.
