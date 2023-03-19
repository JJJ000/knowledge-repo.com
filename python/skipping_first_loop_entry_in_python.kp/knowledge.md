---
title: How to exclude the first element in a Python for loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the continue statement within the loop to skip the iteration of the first entry.
---

**Contents**

[TOC]

Section 1: Introduction
For loops are widely used in python programming for iterating over a sequence such as a list, tuple, set or dictionary. There may be instances where we want to skip the first entry in a for loop. In this article, we will discuss how to skip the first entry in a for loop in python.

Section 2: Using range function to skip first entry
One way to skip the first entry in a for loop is by using the range function. We can start iterating from the second element onwards and ignore the first element. Here's how we can implement it in python:

```
list1 = ['apple', 'banana', 'cherry', 'orange']

for i in range(1,len(list1)):
    print(list1[i])
```
Output:
```
banana
cherry
orange
```
In the above example, we skipped the first element 'apple' and started iterating from 'banana' onwards.

Section 3: Using enumerate function to skip first entry
Another way to skip the first entry in a for loop is by using the enumerate function. We can use the enumerate function to access the index of each element in the list, and then ignore the first index. Here's how we can implement it in python:

```
list1 = ['apple', 'banana', 'cherry', 'orange']

for i,element in enumerate(list1):
    if i != 0:
        print(element)
```
Output:
```
banana
cherry
orange
```
In the above example, we used the enumerate function to access the index of each element in the list, and then ignored the first index by adding an if condition.

Section 4: Conclusion
In this article, we discussed two ways to skip the first entry in a for loop. We can use the range function or the enumerate function to achieve this. By using these methods, we can easily customize our for loops to suit our needs.
