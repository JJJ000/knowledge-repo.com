---
title: Obtain an array of values corresponding to an array of keys from a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use list comprehension or loop through the keys and extract the corresponding values from the dictionary.
---

**Contents**

[TOC]

## Section 1: Introduction

Python provides a built-in dictionary data structure to hold key-value pairs. There are certain situations where we want to retrieve the values for a list of keys from the dictionary. In this tutorial, we will discuss different ways to get a list of values for the list of keys in Python.

## Section 2: Get values using a for loop

One way to get the list of values for list of keys is by using a for loop.

```python
# initialize dictionary
my_dict = {'apple': 50, 'banana': 20, 'grape': 30, 'mango': 40}

# list of keys to retrieve values
keys_to_retrieve = ['apple', 'grape']

# using for loop
values = []
for key in keys_to_retrieve:
    values.append(my_dict[key])

print(values)
```

Output:
```
[50, 30]
```

In the code snippet above, we have initialized a dictionary `my_dict` with key-value pairs. We have created a list `keys_to_retrieve` that contains keys for which we want to retrieve values. Then we used a for loop to iterate through the list of keys and append the corresponding values to a separate list.

## Section 3: Get values using dictionary comprehension

We can also use dictionary comprehension to retrieve the list of values for a list of keys in a more concise way.

```python
# initialize dictionary
my_dict = {'apple': 50, 'banana': 20, 'grape': 30, 'mango': 40}

# list of keys to retrieve values
keys_to_retrieve = ['apple', 'grape']

# using dictionary comprehension
values = [my_dict[key] for key in keys_to_retrieve]

print(values)
```

Output:
```
[50, 30]
```

In the code snippet above, we have used dictionary comprehension to retrieve the values for the list of keys. The syntax for dictionary comprehension is `{expression for variable in iterable}`. Here, the `expression` is `my_dict[key]` which retrieves the value for the given key. The `variable` is `key` which iterates over the list of keys. The `iterable` is `keys_to_retrieve` which is the list of keys.

## Section 4: Get values using map() function

We can also use the built-in `map()` function to retrieve the list of values for a list of keys.

```python
# initialize dictionary
my_dict = {'apple': 50, 'banana': 20, 'grape': 30, 'mango': 40}

# list of keys to retrieve values
keys_to_retrieve = ['apple', 'grape']

# using map() function
values = list(map(my_dict.get, keys_to_retrieve))

print(values)
```

Output:
```
[50, 30]
```

In the code snippet above, we have used the `map()` function to retrieve the values for the list of keys. The `map()` function applies the `my_dict.get` method to each element of the list `keys_to_retrieve`. The `my_dict.get` method returns the value for the given key. Finally, we have converted the resulting `map` object to a list using the `list()` function.
