---
title: How can we sort a list without considering the case of the items in the list, without converting the result to lowercase?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the key parameter of the sorted function with a lambda function that returns the lowercase version of the string.
---

**Contents**

[TOC]

# Problem Statement

We need to sort a list in a case-insensitive manner in Python, but without actually lowercasing the result.


# Approach

To solve this problem, we can make use of the built-in `sort` method of Python lists. We can pass a `key` parameter to this method that will determine the sorting order.


## Step 1: Creating a List

Let us start by creating a list that we want to sort.

```python
my_list = ['apple', 'banana', 'Cat', 'dog', 'Elephant', 'Frog']
```

## Step 2: Defining the Key Function

To perform case-insensitive sorting, we can define a function that takes a string as input and returns the string in lowercase. We can then pass this function as the `key` parameter to the `sort` method.

```python
def my_key(s):
    return s.lower()
```

## Step 3: Sorting the List

Now that we have our key function defined, we can sort the list using the `sort` method and passing our key function as a parameter.

```python
my_list.sort(key=my_key)
```

## Step 4: Printing the Sorted List

Finally, we can print the sorted list to verify that it has been sorted in a case-insensitive manner.

```python
print(my_list)
```


# Final Code

Putting it all together, we get the following code:

```python
my_list = ['apple', 'banana', 'Cat', 'dog', 'Elephant', 'Frog']

def my_key(s):
    return s.lower()

my_list.sort(key=my_key)

print(my_list)
```

This will output `['apple', 'banana', 'Cat', 'dog', 'Elephant', 'Frog']` which is the original list, but sorted in a case-insensitive manner.
