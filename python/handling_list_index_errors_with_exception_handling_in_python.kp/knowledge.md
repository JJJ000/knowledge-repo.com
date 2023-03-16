---
title: I would like to implement exception handling for 'list index out of range' error
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You can use a try-except block to handle the `list index out of range` exception in Python.
---

**Contents**

[TOC]

## Introduction

When working with lists in Python, you may encounter the error 'list index out of range' when trying to access an index that does not exist in the list. It can be frustrating to encounter this error, especially if you are not sure how to handle it properly. In this tutorial, we will go over how to exception handle 'list index out of range' in Python.

## Using Try-Except Block

One way to handle this error is to use a try-except block. This allows you to catch the error and handle it in a specific way. Below is an example of how to use a try-except block to handle 'list index out of range' error:

```python
my_list = [1, 2, 3]
try: 
    print(my_list[3])
except IndexError:
    print("Index out of range")
```

In this example, we are trying to access an index that does not exist (the index 3) in the list. Instead of encountering an error and stopping the program, the try-except block catches the error and prints out a message that tells the user what went wrong.

## Checking if Index is in Range

Another way to handle this error is to check if the index is in range before trying to access it. In Python, you can use the len() function to get the number of items in a list. Then, you can check if the index is within the range of the list. Below is an example of how to do this:

```python
my_list = [1, 2, 3]
if len(my_list) > 3:
    print(my_list[3])
else:
    print("Index out of range")
```

In this example, we are first checking if the length of the list is greater than 3. If it is, we can safely access the index 3 without encountering an error. If it is not, we print out a message telling the user that the index is out of range.

## Using the 'in' Keyword

Finally, you can use the 'in' keyword in Python to check if an index exists in a list. Below is an example of how to use the 'in' keyword to avoid the 'list index out of range' error:

```python
my_list = [1, 2, 3]
if 3 in my_list:
    print(my_list[3])
else:
    print("Index out of range")
```

In this example, we are checking if the number 3 exists in the list before trying to access it. If it does, we can safely access the index 3 without encountering an error. If it does not, we print out a message telling the user that the index is out of range.

## Conclusion

In conclusion, there are several ways to handle the 'list index out of range' error in Python. You can use a try-except block to catch the error, check if the index is in range before accessing it, or use the 'in' keyword to check if an index exists in a list. By using these methods, you can avoid errors and ensure that your program runs smoothly.
