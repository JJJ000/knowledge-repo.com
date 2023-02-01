---
title: Turn a list into a tuple in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: A tuple can be created from a list by using the tuple() function.
---

**Contents**

[TOC]

# Section 1: What is a Tuple?
A tuple is an immutable sequence of elements. It is similar to a list but each element is immutable, meaning it cannot be changed. Tuples can contain any type of object, including other tuples.

# Section 2: List to Tuple Conversion
To convert a list to a tuple, use the built-in tuple() function. The syntax for this is:

`tuple(list_name)`

For example, to convert the list:

`list_name = [1, 2, 3]`

to a tuple, use the following code:

`tuple_name = tuple(list_name)`

# Section 3: Benefits of Tuples
Tuples offer a number of benefits over lists. Firstly, they are immutable, meaning that their values cannot be changed. This makes them more secure and less prone to errors. Secondly, they are faster than lists. This is because they are stored in a single block of memory, rather than in individual elements as is the case with lists. Finally, tuples are more memory-efficient than lists, as they require less memory to store.

# Section 4: Conclusion
Converting a list to a tuple can be done easily using the built-in tuple() function. Tuples offer a number of benefits over lists, including immutability, faster performance, and more efficient memory usage. Knowing how to convert a list to a tuple can be useful in a variety of programming contexts.
