---
title: Do dict literals and dict constructors have any distinctions or variations?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: No, there is no difference between using a dict literal and a dict constructor in Python.
---

**Contents**

[TOC]

Creation of a Dictionary Literal 

A dictionary literal in Python is declared using curly braces. Inside the braces, comma-separated key-value pairs are defined using colons between the key and the values. For example, {‘key1’: value1, ‘key2’: value2, …}, where key is a string and value can be anything.

Using a Dictionary Constructor 

A dictionary can also be created using a dict constructor. The dict constructor can take one of the following four arguments:

1. An iterable of key-value pairs
2. An iterable of tuples, where each tuple contains two items (key, value)
3. A dictionary
4. Keyword arguments, where the argument names are the keys and the argument values are the values.

Difference between using a Dictionary Literal and Constructor 

1. Performance 
Creating a dictionary literal is faster than creating a dictionary constructor, mainly due to the overhead involved in calling the constructor function.

2. Key Naming 
The keys in the dictionary literal must be valid Python identifiers, whereas keys in the dictionary constructor can be any valid Python objects.

3. Constructor offers more flexibility 
The dictionary constructor is more flexible than the literal in terms of input types. It can accept iterables of key-value pairs, tuples, or even other dictionaries.

4. Positional Arguments 
When using the dictionary constructor, you can pass argument key-value pairs as positional arguments. However, positional arguments are not allowed in dictionary literals. 

Conclusion 

The main difference between using a dictionary literal and a dictionary constructor in Python is performance, key naming, flexibility, and positional arguments. While the dictionary literal is faster and stricter with key naming, the constructor is more flexible, can take key-value pairs as positional arguments, and can accept iterables and other dictionaries.
