---
title: Python code with a lengthy conditional statement
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: It is recommended to avoid very long if statements in Python and instead break them down into smaller, more manageable pieces.
---

**Contents**

[TOC]

Introduction 

In programming, sometimes we come across situations where we need to check multiple conditions at once to establish a certain behavior. In Python, we can use the `if` statement to specify different conditions for different cases. However, when we have too many conditions to check, the `if` statement can become very long and hard to read. In this article, we will discuss how to handle very long `if` statements in Python.

1. Splitting the if statement

One way to handle a long if statement is to break it up into several smaller if statements. We can split up the long if statement into several shorter if statements and use logical operators to combine them. For example, instead of writing:

```python
if condition1 and condition2 and condition3 and condition4 and condition5 and condition6:
    do_something()
```

We can split it up into:

```python
if condition1 and condition2:
    if condition3 and condition4:
        if condition5 and condition6:
            do_something()
```
This makes the code more readable and easier to understand.

2. Using the any() and all() functions

Another way to handle a long if statement is to use the `any()` and `all()` functions in Python. These functions take one or more iterables as arguments and return `True` or `False` depending on whether any or all of the elements in the iterable evaluate to `True`.

For example, instead of writing:

```python
if condition1 or condition2 or condition3 or condition4:
    do_something()
```

We can use the `any()` function as follows:

```python
if any([condition1, condition2, condition3, condition4]):
    do_something()
```

And instead of writing:

```python
if condition1 and condition2 and condition3 and condition4:
    do_something()
```

We can use the `all()` function as follows:

```python
if all([condition1, condition2, condition3, condition4]):
    do_something()
```

This way, we can check all the conditions and make the code more concise and readable.

3. Using a dictionary

Another way to handle a long if statement is by using a dictionary. We can create a dictionary where the keys represent the conditions and the values represent the corresponding actions. For example:

```python
conditions = {
    condition1: do_something1,
    condition2: do_something2,
    condition3: do_something3,
    condition4: do_something4,
    ...
}

for condition, action in conditions.items():
    if condition:
        action()
```

This way, we can check all conditions and perform the corresponding action without having to write a long if statement.

4. Using a function

Lastly, we can handle a long if statement by creating a function. We can define the function with the conditions and actions as arguments and call the function instead of the long if statement. For example:

```python
def perform_action(condition1, condition2, condition3, condition4):
    if condition1:
        do_something1()
    if condition2:
        do_something2()
    if condition3:
        do_something3()
    if condition4:
        do_something4()

perform_action(condition1, condition2, condition3, condition4)
```

This way, we can group the conditions and actions together and make the code more modular and easier to test.

Conclusion 

In this article, we discussed how to handle very long if statements in Python. By splitting the if statement, using the any() and all() functions, using a dictionary or creating a function, we can make the code more concise, readable, and easier to understand.
