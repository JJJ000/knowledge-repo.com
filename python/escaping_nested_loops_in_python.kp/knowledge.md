---
title: Escaping from multiple levels of loops
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `break` keyword to exit out of the innermost loop.
---

**Contents**

[TOC]

**Breaking Out of a Single Nested Loop**

Python provides an easy way to break out of a single nested loop using the `break` keyword. For example, the following code will loop through a list of numbers, and break out of the loop if the number is greater than 10:

```python
for i in range(20):
    for j in range(i):
        if j > 10:
            break
        print(j)
```

**Breaking Out of Multiple Nested Loops**

Breaking out of multiple nested loops is slightly more complicated. One way to do this is to use a `flag` variable. The flag variable is used to indicate when the loop should be broken out of. For example, the following code will loop through a list of numbers, and break out of two nested loops if the number is greater than 10:

```python
flag = False
for i in range(20):
    for j in range(i):
        if j > 10:
            flag = True
            break
        print(j)
    if flag:
        break
```

**Using Labels to Break Out of Multiple Nested Loops**

Another way to break out of multiple nested loops is to use labels. Labels are used to identify a loop, and can be used with the `break` keyword to break out of multiple nested loops. For example, the following code will loop through a list of numbers, and break out of two nested loops if the number is greater than 10:

```python
outer_loop:
for i in range(20):
    for j in range(i):
        if j > 10:
            break outer_loop
        print(j)
```

**Using Exceptions to Break Out of Multiple Nested Loops**

The last way to break out of multiple nested loops is to use exceptions. Exceptions are used to indicate an error or unexpected behavior in a program. For example, the following code will loop through a list of numbers, and break out of two nested loops if the number is greater than 10:

```python
try:
    for i in range(20):
        for j in range(i):
            if j > 10:
                raise Exception('Number is greater than 10')
            print(j)
except Exception as e:
    print(e)
```
