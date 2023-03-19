---
title: Can iterating over two lists be improved by obtaining one element from each list in every iteration?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Yes, use the built-in function zip() to iterate over two lists simultaneously.
---

**Contents**

[TOC]

Section 1: The Classic Approach 
One approach to iterating over two lists in Python is to use the built-in zip() function, which returns an iterator of tuples pairing elements from each input sequence. The classic approach is to use a for loop and iterate over the returned tuples-from-zip for each iteration. 

```python
list1 = ['a', 'b', 'c']
list2 = [1, 2, 3]

for (x, y) in zip(list1, list2):
    # do something with x and y
    print(x, y)
``` 

Section 2: Alternatives to zip() 
Although zip() is a convenient method for pairing elements from lists, it might not always be the best approach depending on the application. For example, if the two input lists are different lengths, the zip() function will truncate the longer list to match the shorter list. Alternatively, if one of the lists is already large, converting the other list to a tuple and zipping it can be memory-intensive. Some alternative methods to zip() include using itertools.product() or itertools.chain(). 

```python
import itertools

list1 = ['a', 'b', 'c']
list2 = [1, 2, 3]

# Using itertools.product() creates an iterator 
# that returns the Cartesian product of inputs
for (x, y) in itertools.product(list1, list2):
    # do something with x and y
    print(x, y)

# Using itertools.chain() allows you to merge
# any number of input iterables 
for item in itertools.chain(list1, list2):
    # do something with item
    print(item)
``` 

Section 3: Pythonsic Approach 
A more pythonic way to iterate over two lists is to use the list comprehension, which is considered more pythonic for its compactness and readability of the code, thus you get the cartesian product or pairs of the two lists.

```python
list1 = ['a', 'b', 'c']
list2 = [1, 2, 3]

pairs = [(x,y) for x in list1 for y in list2]
# do something with pairs
print(pairs)
```

Here we go, with few of the most common methods to iterate over the two lists, depending on the use case one approach might definitively be better than the other.
