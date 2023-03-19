---
title: What is the method to verify if any of the enumerated elements exists in a given list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `in` keyword followed by the list name and the item you want to check.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, there are different ways to check if a certain item is present in a list or not. This is a common task in many programming projects, and there are built-in functions and methods that can help us accomplish it. In this article, we will explore some of these methods and how to use them effectively.

Section 2: Using the 'in' Operator
One of the simplest and most direct ways to check if an item is in a list in Python is by using the 'in' operator. This operator checks whether a certain value exists in a sequence or not, and it returns a Boolean value (True or False) as the result. Here is an example code snippet that explains how to use the 'in' operator to check if an item is in a list:

```python
my_list = ['apple', 'banana', 'orange']
if 'banana' in my_list:
    print("Yes, 'banana' is in the list.")
else:
    print("No, 'banana' is not in the list.")
```

In this example, we create a list called 'my_list' that contains three fruits. We then use the 'in' operator to check if the string 'banana' exists in this list. Since 'banana' is one of the items in the list, the first branch of the if-else statement is executed, and we get the output "Yes, 'banana' is in the list."

Section 3: Using the index() Method
Another way to check if an item is in a list and get its index in the list is by using the index() method. This method returns the index of the first occurrence of a value in a list, or it raises a ValueError exception if the value is not found. Here is an example code snippet that explains how to use the index() method:

```python
my_list = ['apple', 'banana', 'orange']
if 'banana' in my_list:
    index = my_list.index('banana')
    print(f"Yes, 'banana' is in the list at index {index}.")
else:
    print("No, 'banana' is not in the list.")
```

In this example, we create the same list as before, and we use the 'in' operator to check if the string 'banana' exists in the list. If it does, we call the index() method with the argument 'banana' to get the index of the first occurrence of 'banana' in the list. We then print a message that confirms the presence of 'banana' in the list and its index.

Section 4: Using the count() Method
A third way to check if an item is in a list is by using the count() method. This method returns the number of times a value appears in a list, so we can use it to check whether an item is present or not (if the count is greater than zero). Here is an example code snippet that explains how to use the count() method:

```python
my_list = ['apple', 'banana', 'orange']
count = my_list.count('banana')
if count > 0:
    print(f"Yes, 'banana' is in the list {count} times.")
else:
    print("No, 'banana' is not in the list.")
```

In this example, we create the same list as before, and we call the count() method with the argument 'banana' to get the number of occurrences of 'banana' in the list. If the count is greater than zero, we print a message that confirms the presence of 'banana' in the list and its count. Otherwise, we print a message that confirms the absence of 'banana' in the list.
