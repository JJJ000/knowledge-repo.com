---
title: What would be the most effective approach to incorporating nested dictionaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The best way to implement nested dictionaries in Python is by creating a dictionary within a dictionary using curly braces and square brackets.
---

**Contents**

[TOC]

## 1. Creating a Nested Dictionary

To create a nested dictionary in Python, one must first create the outer dictionary and then add inner dictionaries as its values. Here's an example:

```python
my_dict = {
   "fruit": {
       "apple": 2,
       "banana": 3,
       "orange": 4
   },
   "vegetable": {
       "carrot": 1,
       "spinach": 2,
       "celery": 3
   }
}
```

In this example, we created a dictionary named `my_dict` with two nested dictionaries named "fruit" and "vegetable" as its values.

## 2. Accessing Nested Dictionaries

To access the values in a nested dictionary, one can use square brackets to access each level of the dictionary. Here's an example:

```python
#accessing the value of 'apple' in 'fruit'
print(my_dict['fruit']['apple']) 
#output: 2

#accessing the value of 'spinach' in 'vegetable'
print(my_dict['vegetable']['spinach']) 
#output: 2
```

## 3. Adding or Modifying Nested Dictionaries

Adding a new nested dictionary or modifying an existing one is just like modifying any other dictionary. Here's an example:

```python
#adding a new nested dictionary
my_dict["meat"] = {
    "beef": 2,
    "chicken": 3,
    "pork": 4
}

#modifying an existing nested dictionary
my_dict['fruit']['apple'] = 5
```

In this example, we added a new nested dictionary under the key "meat" and modified the value of "apple" under the nested dictionary "fruit."

## 4. Removing Nested Dictionaries

Removing a nested dictionary from a parent dictionary is also simple. Here's an example:

```python
#removing the nested dictionary under the key 'vegetable'
del my_dict['vegetable']
```

In this example, we deleted the nested dictionary under the key "vegetable" using the Python del keyword.
