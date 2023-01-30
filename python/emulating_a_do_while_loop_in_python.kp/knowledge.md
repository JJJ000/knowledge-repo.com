---
title: What is the process for imitating a do-while loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: A do-while loop can be emulated in Python using a while loop with a True condition and a break statement.
---

**Contents**

[TOC]

**Using a While Loop**

1. Initialize the variable that will be used in the loop condition:
    ```python
    x = 0
    ```

2. Create the while loop:
    ```python
    while True:
        # code to be executed
        x += 1
    ```

3. Use a break statement to exit the loop when the condition is met:
    ```python
    if x > 5:
        break
    ```

**Using a For Loop**

1. Initialize the variable that will be used in the loop condition:
    ```python
    x = 0
    ```

2. Create the for loop:
    ```python
    for x in range(6):
        # code to be executed
    ```

3. Use a break statement to exit the loop when the condition is met:
    ```python
    if x == 5:
        break
    ```
