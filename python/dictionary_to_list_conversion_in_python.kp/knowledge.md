---
title: How can a dictionary be transformed into a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To convert a dictionary to a list in Python, use the built-in function list() and pass in the dictionary as an argument.
---

**Contents**

[TOC]

Section 1: Introduction to Dictionaries and Lists

In Python, dictionaries and lists are two commonly used data structures. 

Dictionaries use a key-value pair system, where each key maps to a unique value. The keys in a dictionary must be unique, immutable objects, while the values can be of any data type. 

Lists, on the other hand, are ordered collections of objects. The objects in a list can be of any type and can be repeated. Lists can also be nested (i.e. a list within a list). 

In this tutorial, we will discuss how to convert a dictionary to a list in Python.

Section 2: Converting a Dictionary to a List using the items() method

One way to convert a dictionary to a list is by using the items() method. The items() method returns a list of key-value pairs in the form of tuples.

Here is an example:

```
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_list = list(my_dict.items())
print(my_list)
```

Output:

```
[('a', 1), ('b', 2), ('c', 3)]
```

In this example, we use the items() method to get a list of key-value pairs from the dictionary. We then use the built-in list() function to convert this list of tuples to a list.

Section 3: Converting a Dictionary to a List using List Comprehension

Another way to convert a dictionary to a list is by using list comprehension. Here is an example:

```
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_list = [(key, value) for key, value in my_dict.items()]
print(my_list)
```

Output:

```
[('a', 1), ('b', 2), ('c', 3)]
```

In this example, we use list comprehension to create a list of tuples containing the key-value pairs from the dictionary.

Section 4: Conclusion

Converting a dictionary to a list in Python is a useful skill to have. It allows us to manipulate the elements of a dictionary as a list, which can be useful in many situations. In this tutorial, we discussed two methods for converting a dictionary to a list: using the items() method and using list comprehension.
