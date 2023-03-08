---
title: What is the method for adding an integer to every item in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can use list comprehension to add the integer to each element in the list [x + integer for x in my\_list].
---

**Contents**

[TOC]

## Getting Started
Before we begin with the solution, we need to make sure that we have a basic understanding of Python lists, arithmetic operations, and loops.

To add an integer to each element in a list, we can use a for loop to iterate over each element and add the integer to it. 

Now, let's get started with the solution.

## Solution Approach
We can add an integer to each element in a list using a for loop, and the += operator. The += operator allows us to add a value to a variable and then assign the result back to the same variable. 

Here's how we can add an integer, say 2, to each element in a list.

```python
original_list = [1, 2, 3, 4, 5]
integer_to_add = 2

for i in range(len(original_list)):
    original_list[i] += integer_to_add

print(original_list)
```

## Output
The above code will output the following list:

```python
[3, 4, 5, 6, 7]
```

## Conclusion
In this solution, we used a for loop and the += operator to add an integer to each element in a list. This can be useful when we want to modify the original list without creating a new list or when we want to perform some arithmetic operations on the elements of the list.
