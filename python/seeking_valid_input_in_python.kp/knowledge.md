---
title: Requesting input from the user until a satisfactory answer is provided
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Keep asking the user for input until they give a valid response by using a while loop and an if statement.
---

**Contents**

[TOC]

### 1. Defining a Valid Response

Before asking the user for input, it is important to define what is considered a valid response. This could be a specific type of data (e.g. a number or a string), or it could be a specific value (e.g. yes or no).

### 2. Asking for Input

Once the valid response is defined, the user can be asked for input. This can be done using the `input()` function, which will prompt the user to enter a response.

### 3. Evaluating the Response

The user's response can then be evaluated to determine if it is a valid response. This can be done using an `if` statement and the `type()` function to check the data type of the response, or by comparing the response to the valid value.

### 4. Looping Until Valid Response

If the user's response is not valid, the program can loop back to the `input()` function until a valid response is given. This can be done using a `while` loop, which will continue to loop until the user's response is valid.
