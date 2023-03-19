---
title: Perform x if the index of the list is present
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Check if the index exists using the `in` keyword and perform the action X if it does.
---

**Contents**

[TOC]

1. Introduction
In Python, we often need to check if a particular index exists in the list or not. Depending on the existence of the index, we might need to perform different operations. In this article, we will discuss various ways to check if list index exists and what to do if it exists.

2. Using the `in` keyword
The easiest way to check if an index exists in the list is by using the `in` keyword. We can use this keyword to check if a particular value exists in the list or not. If the index exists, we can perform our desired operation, otherwise, we can handle the situation accordingly. Here is an example:

```
my_list = ['apple', 'banana', 'cherry']
if 1 in range(len(my_list)):
    print(my_list[1])  # Output: banana
else:
    print('Index does not exist')
```

In the above example, we have used the `in` keyword to check if the index `1` exists in the list or not. Since the index `1` exists in `my_list`, the program will print the value at that index, which is `banana`.

3. Using exception handling
Another way to check if the index exists in the list is by using exception handling. We can use `try` and `except` blocks to handle the situation where the index does not exist in the list. Here is an example:

```
my_list = ['apple', 'banana', 'cherry']
try:
    value = my_list[3]
    print(value)
except IndexError:
    print('Index does not exist')
```

In the above example, we have used a `try` block to access the value at index `3` in `my_list`. Since there is no index `3` in `my_list`, an `IndexError` exception will be raised. We have used the `except` block to handle this exception and print a message that says the index does not exist.

4. Using the len() function
We can also use the `len()` function to check if the index exists in the list or not. We can check if the given index is less than the length of the list or not. Here is an example:

```
my_list = ['apple', 'banana', 'cherry']
if 3 < len(my_list):
    print(my_list[3])
else:
    print('Index does not exist')
```

In the above example, we have used the `len()` function to get the length of `my_list`. We have then checked if the index `3` is less than the length of the list. Since index `3` does not exist in `my_list`, the program will print a message that says the index does not exist.

5. Conclusion
In this article, we have discussed various ways to check if list index exists or not in Python. We have seen that we can use the `in` keyword, exception handling, and the `len()` function to check if the index exists in the list or not. Depending on the existence of the index, we can perform different operations to handle the situation.
