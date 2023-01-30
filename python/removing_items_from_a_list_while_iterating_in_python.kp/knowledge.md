---
title: What is the process for deleting elements from a list as it is being looped through?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use a for loop with an if statement to iterate through the list and remove items that meet certain criteria.
---

**Contents**

[TOC]

### Using a For Loop

The easiest way to remove items from a list while iterating is to use a `for` loop. The `for` loop will iterate over each item in the list and check if it meets a certain criteria. If it does, then the item can be removed from the list. 

```python
my_list = [1,2,3,4,5,6]

for item in my_list:
    if item % 2 == 0:
        my_list.remove(item)

print(my_list) # [1, 3, 5]
```

In the example above, the `for` loop iterates over each item in the list and checks if it is an even number. If it is, then it is removed from the list.

### Using List Comprehension

Another way to remove items from a list while iterating is to use list comprehension. List comprehension is a concise way of creating lists by evaluating an expression. 

```python
my_list = [1,2,3,4,5,6]

my_list = [item for item in my_list if item % 2 != 0]

print(my_list) # [1, 3, 5]
```

In the example above, the list comprehension evaluates the expression `item for item in my_list if item % 2 != 0` for each item in the list. This expression checks if the item is an odd number and if it is, it is added to the new list.

### Using Filter

A third way to remove items from a list while iterating is to use the `filter()` function. The `filter()` function takes a function and a list as arguments and returns a new list with only the elements that pass the given function. 

```python
my_list = [1,2,3,4,5,6]

def is_odd(num):
    return num % 2 != 0

my_list = filter(is_odd, my_list)

print(list(my_list)) # [1, 3, 5]
```

In the example above, the `filter()` function takes a function `is_odd` and a list `my_list` as arguments. The `is_odd` function checks if the item is an odd number and if it is, it is added to the new list.

### Using a While Loop

The last way to remove items from a list while iterating is to use a `while` loop. The `while` loop will iterate over each item in the list and check if it meets a certain criteria. If it does, then the item can be removed from the list. 

```python
my_list = [1,2,3,4,5,6]

i = 0
while i < len(my_list):
    if my_list[i] % 2 == 0:
        my_list.remove(my_list[i])
    else:
        i += 1

print(my_list) # [1, 3, 5]
```

In the example above, the `while` loop iterates over each item in the list and checks if it is an even number. If it is, then it is removed from the list. The `i` variable is used to keep track of the index of the list so that the loop does not skip any items.
