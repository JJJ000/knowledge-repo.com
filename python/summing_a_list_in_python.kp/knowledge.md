---
title: Calculate the total of a list of numbers in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Sum the numbers in the list by using the built-in sum() function.
---

**Contents**

[TOC]

#Solution 1: Using a for loop

```python
def sum_numbers(numbers):
    total = 0
    for num in numbers:
        total += num
    return total

numbers = [1, 2, 3, 4, 5]
print(sum_numbers(numbers)) # Output: 15
```

#Solution 2: Using built-in functions

```python
def sum_numbers(numbers): 
    return sum(numbers) 
  
numbers = [1, 2, 3, 4, 5]
print(sum_numbers(numbers)) # Output: 15
```

#Solution 3: Using a while loop

```python
def sum_numbers(numbers): 
    total = 0
    i = 0
    while i < len(numbers):
        total += numbers[i]
        i += 1
    return total

numbers = [1, 2, 3, 4, 5]
print(sum_numbers(numbers)) # Output: 15
```

#Solution 4: Using recursion

```python
def sum_numbers(numbers):
    if len(numbers) == 1:
        return numbers[0]
    else:
        return numbers[0] + sum_numbers(numbers[1:])

numbers = [1, 2, 3, 4, 5]
print(sum_numbers(numbers)) # Output: 15
```
