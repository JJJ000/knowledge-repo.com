---
title: What is the procedure for building a set from a list of items in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the set() function to convert a list to a set in Python.
---

**Contents**

[TOC]

# 1. Introduction

Sets are an unordered collection of unique elements in Python. They can be constructed from any iterable object, such as a list or a tuple.

In this tutorial, we will explore how to construct a set from a list in Python.

# 2. Converting a List to a Set

To convert a list to a set in Python, we can use the built-in set() function. The set() function takes an iterable (in this case, a list) as input and returns a set that contains all the unique elements of the iterable.

Here's an example:

```python
my_list = [1, 2, 3, 3, 4, 4, 5]
my_set = set(my_list)
print(my_set)
```

Output:

```
{1, 2, 3, 4, 5}
```

As you can see, we have created a set that contains all the elements of the original list, but with all duplicates removed.

# 3. Creating an Empty Set and Adding Elements

We can also create an empty set and add elements to it using the set() function. This can be useful when we want to construct a set based on some condition or algorithm.

Here's an example:

```python
my_set = set()
my_list = [1, 2, 3, 3, 4, 4, 5]

for i in my_list:
    if i % 2 == 0:
        my_set.add(i)

print(my_set)
```

Output: 

```
{2, 4}
```

In this example, we have created an empty set called my_set and added all even numbers from the original list to it using the add() method.

# 4. Conclusion

In this tutorial, we have seen how to construct a set from a list in Python using the set() function. We have also learned how to create an empty set and add elements to it based on some condition or algorithm. Sets are a powerful data structure in Python, and they can be used in a variety of applications, such as removing duplicates from a list and checking for intersection or union between two sets.
