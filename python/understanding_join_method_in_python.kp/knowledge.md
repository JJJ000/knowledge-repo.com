---
title: Could you provide a precise explanation of the function of the .join() method?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The .join() method is used to concatenate a list of strings into a single string with a specified separator character.
---

**Contents**

[TOC]

## Overview
The `.join()` method is a string method in Python that creates a new string by concatenating elements from an iterable object. The iterable object can be a list, tuple, set, string, or any other sequence type that can be iterated over. The method takes one argument, which is the iterable object that needs to be joined.

## The syntax of the .join() method
The syntax for using the `.join()` method in Python is as follows:

```python
new_string = separator.join(iterable)
```

Here, `separator` is an optional string that is used to separate the elements in the iterable object. If it is not specified, the default separator used is an empty string. `iterable` is the iterable object that needs to be joined to create a new string.

## Examples
Here are some examples that illustrate the usage of the `.join()` method in Python:

```python
# Joining strings using .join() method

words = ['Python', 'is', 'awesome']
sentence = ' '.join(words)
print(sentence)   # Output: Python is awesome

# Joining tuple elements using .join() method

numbers = (1, 2, 3, 4)
num_str = ''.join(str(i) for i in numbers)
print(num_str)    # Output: 1234

# Joining set elements using .join() method

fruits = {'apple', 'banana', 'kiwi'}
fruits_str = ', '.join(fruits)
print(fruits_str) # Output: kiwi, banana, apple
```

In the first example, we join the elements of the `words` list using a space separator. In the second example, we join the elements of the `numbers` tuple to create a string of numbers. In the third example, we join the elements of the `fruits` set using a comma and space separator.
