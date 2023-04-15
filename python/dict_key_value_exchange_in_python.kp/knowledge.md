---
title: What's the procedure for swapping dictionary keys with their values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can use a dictionary comprehension to swap keys and values in a dictionary.
---

**Contents**

[TOC]

## Introduction
A Python dictionary is a collection of key-value pairs, where each key maps to a particular value. Sometimes we may need to exchange the keys with their corresponding values in a dictionary. In this article, we will discuss some ways to achieve this in Python.

## Method 1: Using Dictionary Comprehension
One way to exchange keys with values in a dictionary is to use dictionary comprehension. In this method, we iterate over the key-value pairs of the original dictionary and create a new dictionary with the keys and values exchanged.

```python
# create a dictionary
my_dict = {'apple': 1, 'banana': 2, 'cherry': 3}

# exchange keys with values using dictionary comprehension
new_dict = {v: k for k, v in my_dict.items()}

# print the new dictionary
print(new_dict) # output: {1: 'apple', 2: 'banana', 3: 'cherry'}
```

## Method 2: Using zip() Function and dict()
Another way to exchange keys with values in a dictionary is to use the zip() function and the dict() constructor. The zip() function takes two or more sequences and returns a tuple of their corresponding elements. In this method, we use zip() function to create a sequence of tuples with the values as the first element and the keys as the second element. Then we pass this sequence to the dict() constructor to create a new dictionary with keys and values exchanged.

```python
# create a dictionary
my_dict = {'apple': 1, 'banana': 2, 'cherry': 3}

# exchange keys with values using zip() function and dict() constructor
new_dict = dict(zip(my_dict.values(), my_dict.keys()))

# print the new dictionary
print(new_dict) # output: {1: 'apple', 2: 'banana', 3: 'cherry'}
```

## Method 3: Using a For Loop
We can also exchange keys with values in a dictionary using a for loop. In this method, we iterate over the key-value pairs of the original dictionary and add the key-value pairs to a new dictionary with the keys and values exchanged.

```python
# create a dictionary
my_dict = {'apple': 1, 'banana': 2, 'cherry': 3}

# exchange keys with values using a for loop
new_dict = {}
for key, value in my_dict.items():
    new_dict[value] = key

# print the new dictionary
print(new_dict) # output: {1: 'apple', 2: 'banana', 3: 'cherry'}
```

## Conclusion
In this article, we discussed some ways to exchange keys with values in a dictionary in Python. We learned how to use dictionary comprehension, zip() function and dict() constructor, and a for loop to achieve this. These methods can come in handy while working with dictionaries in Python.
