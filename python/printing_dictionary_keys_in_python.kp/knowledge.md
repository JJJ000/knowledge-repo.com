---
title: What is the method to obtain the key of a dictionary through printing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To print a dictionary`s keys in Python, use the keys() method.
---

**Contents**

[TOC]

# Introduction
Printing a dictionary's key is a common task in Python. In this tutorial, we will explore different ways to achieve this task in Python.

# Creating a dictionary
Before printing the keys of a dictionary, we need to create a dictionary. We can create a dictionary by using the curly braces {} or by using the dict() constructor function.

# Method 1: Using a for loop
We can use a for loop to print the keys of a dictionary. Here is an example:

```
my_dict = {'name': 'John', 'age': 25, 'gender': 'male'}
for key in my_dict:
    print(key)
```

Output:
```
name
age
gender
```

In the above example, we use a for loop to iterate over the keys of the dictionary and print them.

# Method 2: Using the keys() function
We can also use the keys() function to get a list of keys of a dictionary and then print them. Here is an example:

```
my_dict = {'name': 'John', 'age': 25, 'gender': 'male'}
keys = my_dict.keys()
for key in keys:
    print(key)
```

Output:
```
name
age
gender
```

In the above example, we use the keys() function to get a list of keys of the dictionary and then use a for loop to iterate over the keys and print them.

# Method 3: Converting to a list
We can also convert the keys of a dictionary to a list and print them. Here is an example:

```
my_dict = {'name': 'John', 'age': 25, 'gender': 'male'}
keys = list(my_dict)
for key in keys:
    print(key)
```

Output:
```
name
age
gender
```

In the above example, we convert the dictionary keys to a list using the list() function and then use a for loop to iterate over the keys and print them.
