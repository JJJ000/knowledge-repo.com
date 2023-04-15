---
title: How to count the elements in a Python list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To count elements in a list in Python, use the len() function on the list.
---

**Contents**

[TOC]

Counting Elements in a Python List

Introduction
When working with data structures in Python, it is often necessary to count the number of elements in a list. The number of elements in a list is also known as its length. The length of a list can be determined using various built-in functions provided by Python.

Using the Built-in len() Function

One of the easiest ways to count the elements in a Python list is to use the built-in len() function. The len() function is a built-in Python function that takes an iterable object as its argument and returns the number of elements in the object. We can pass the list to the len() function to get its length.

Example code:

list1 = [1, 2, 3, 4, 5]
list2 = ["apple", "banana", "orange"]
list3 = []
print(len(list1))   # Output: 5
print(len(list2))   # Output: 3
print(len(list3))   # Output: 0

Using a For Loop

Another way to count the elements in a Python list is to use a for loop. We can iterate through the list and increment a counter variable for each element in the list. Once we have iterated through the entire list, the counter variable will contain the total number of elements in the list.

Example code:

list1 = [1, 2, 3, 4, 5]
list2 = ["apple", "banana", "orange"]
list3 = []
count1 = count2 = count3 = 0
for i in list1:
    count1 += 1
for j in list2:
    count2 += 1
for k in list3:
    count3 += 1
print(count1)   # Output: 5
print(count2)   # Output: 3
print(count3)   # Output: 0

Using List Comprehension

We can also use list comprehension to count the elements in a Python list. List comprehension is a concise way to create lists based on existing lists. We can use list comprehension to generate a list of 1s, where the number of 1s in the list is equal to the number of elements in the original list. We can then use the built-in sum() function to add up all the 1s in the list, giving us the total number of elements in the original list.

Example code:

list1 = [1, 2, 3, 4, 5]
list2 = ["apple", "banana", "orange"]
list3 = []
count1 = sum([1 for i in list1])
count2 = sum([1 for j in list2])
count3 = sum([1 for k in list3])
print(count1)   # Output: 5
print(count2)   # Output: 3
print(count3)   # Output: 0

Conclusion

In this tutorial, we have explored three different ways to count the elements in a Python list. We can use the built-in len() function, a for loop, or list comprehension to obtain the total length of a list. These techniques can be used in various programming scenarios where it is important to know the number of elements in a list.
