---
title: Search for and substitute string values in a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use a list comprehension with a conditional statement to replace the string values with the new value.
---

**Contents**

[TOC]

# Introduction
In programming, when working with a list, there are times when you need to find and replace specific string values with new string values. This can be easily accomplished in Python using simple code.

# Method 1: for loop
One way to find and replace string values in a list is by using a for loop. Here's how to do it:

```
my_list = ['apple', 'banana', 'orange']
for i in range(len(my_list)):
    if my_list[i] == 'banana':
        my_list[i] = 'grapefruit'
print(my_list)
```

Output:
```
['apple', 'grapefruit', 'orange']
```
In this code, we loop through the list and replace the value 'banana' with 'grapefruit' when we find it. The `len()` function gives us the total number of items in the list, and the `range()` function generates a sequence of numbers from 0 to `len(my_list)-1`. We check for the string value using an `if` statement.

# Method 2: list comprehension
Another approach to replace string values in a list is by using list comprehension. Here's an example:

```
my_list = ['apple', 'banana', 'orange']
new_list = ['grapefruit' if i=='banana' else i for i in my_list]
print(new_list)
```

Output:
```
['apple', 'grapefruit', 'orange']
```

In this code, we create a new list by iterating through the original list `my_list`. We replace the value 'banana' with 'grapefruit' by using a conditional expression inside the list comprehension. The `else` keyword specifies what to do for the items that don't match the condition.

# Method 3: map()
A third way to replace string values in a list is by using the built-in `map()` function. Here's how it works:

```
my_list = ['apple', 'banana', 'orange']
new_list = list(map(lambda x: 'grapefruit' if x=='banana' else x, my_list))
print(new_list)
```

Output:
```
['apple', 'grapefruit', 'orange']
```

In this code, we use the `lambda` function to define the conditional expression. The `map()` function applies the `lambda` function to every element in the list `my_list`, and the `list()` function converts the result to a list.

# Conclusion
In Python, there are multiple ways to find and replace string values in a list. You can use a for loop, list comprehension, or the `map()` function. Choose the method that you prefer based on your specific use case.
