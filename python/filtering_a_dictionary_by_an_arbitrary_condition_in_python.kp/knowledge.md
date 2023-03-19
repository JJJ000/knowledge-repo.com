---
title: What is the method of filtering a dictionary based on a condition function that is arbitrary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use dictionary comprehension with the condition function as the filtering condition.
---

**Contents**

[TOC]

## Section 1: Introduction
In Python, dictionaries are a widely used data structure that stores key:value pairs. Often, we may want to filter a dictionary based on some condition, such as only keeping the key:value pairs where the value meets a certain criteria. This can be achieved by using the built-in `filter()` function paired with a lambda function that defines the condition.

## Section 2: Using the filter() function
The `filter()` function takes a function and an iterable as arguments, and returns a filter object that contains only the elements from the iterable that pass the function's test. In our case, the iterable will be a dictionary, and the function will be a lambda function that defines the condition we want to filter by.

## Section 3: Defining the condition function
Before we can use `filter()`, we need to define the lambda function that will evaluate our filtering condition. The lambda function will take a key:value pair as input, and return `True` if the value meets our criteria, and `False` otherwise. For example, if we want to filter out any key:value pairs where the value is less than 10, we would define our lambda function like so:

```python
condition = lambda key_val: key_val[1] >= 10
```

This lambda function takes a key:value pair as input (in the form of a tuple), and returns `True` if the second element of that tuple (i.e. the value) is greater than or equal to 10.

## Section 4: Filtering the dictionary
Now that we have our lambda function defined, we can use `filter()` to create a new dictionary that only contains the key:value pairs that meet our filtering condition. We can do this by passing the lambda function and our original dictionary to the `filter()` function, and then converting the resulting filter object back into a dictionary using the `dict()` constructor. For example:

```python
my_dict = {'a': 5, 'b': 10, 'c': 15, 'd': 20}

condition = lambda key_val: key_val[1] >= 10

filtered_dict = dict(filter(condition, my_dict.items()))

print(filtered_dict)
```

This will output:

```
{'b': 10, 'c': 15, 'd': 20}
```

which is a new dictionary that only contains the key:value pairs where the value is greater than or equal to 10.
