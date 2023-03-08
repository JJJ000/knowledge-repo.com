---
title: Advancing to the next iteration in the outer loop in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To continue to next iteration in outer loop in Python, one needs to use the continue statement.
---

**Contents**

[TOC]

Section 1: Basic concept
In Python, we can use the 'continue' keyword to skip the current iteration of a loop and continue with the next iteration. However, if we want to skip the current iteration of an outer loop and continue with the next iteration of that outer loop, we need to use a labeled continue statement.

Section 2: Using a labeled continue statement
To use a labeled continue statement in Python, we first need to label the outer loop using the 'label:' syntax. Then, we can use the 'continue label' statement within the inner loop to skip the current iteration of the outer loop and continue with the next iteration of that outer loop.

```
for i in range(5):
    for j in range(5):
        if j == 2:
            continue
        print(i, j)
```
In this example, the inner loop will skip the value of j when it is equal to 2, but it will continue with the next iteration of the inner loop. To skip the current iteration of the outer loop when j is equal to 2, we can label the outer loop and use a labeled continue statement:
```
for i in range(5):
    for j in range(5):
        if j == 2:
            continue i
        print(i, j)
```
In this example, we label the outer loop as 'i', and use 'continue i' within the inner loop to skip the current iteration of the outer loop when j is equal to 2.

Section 3: Using a boolean flag
Another way to skip the current iteration of an outer loop in Python is to use a boolean flag. We can set the flag to True when we want to skip the current iteration of the outer loop, and then check the flag at the end of the inner loop to see if we need to skip the next iteration of the outer loop.

```
for i in range(5):
    skip_i = False
    for j in range(5):
        if j == 2:
            skip_i = True
        else:
            print(i, j)
    if skip_i:
        continue
```
In this example, we initialize the boolean flag 'skip_i' to False before the inner loop starts. If j is equal to 2, we set 'skip_i' to True. At the end of the inner loop, we check 'skip_i', and if it is True, we use 'continue' to skip the next iteration of the outer loop.

Section 4: Conclusion
In summary, we can skip the current iteration of an outer loop in Python by using a labeled continue statement or a boolean flag. The labeled continue statement allows us to skip the current iteration of the outer loop from within the inner loop, while the boolean flag requires us to check the flag at the end of the inner loop to determine if we need to skip the next iteration of the outer loop.
