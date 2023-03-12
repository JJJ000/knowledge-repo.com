---
title: What is the process for calculating the modulus result of a divided by b using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the modulo operator (%) in Python to calculate a mod b.
---

**Contents**

[TOC]

## Introduction
In Python, you can calculate a mod b using the modulus operator (%). The modulus operator returns the remainder when one number is divided by another. This is a very simple solution, but there are a few things to keep in mind.

## Code
Here's an example of how to calculate a mod b in Python:

``` python
a = 10
b = 3
result = a % b
print(result) # Output: 1
```

In this example, we assign 10 to variable `a` and 3 to variable `b`. Then, we use the modulus operator to get the remainder of `a` divided by `b` and assign it to the variable `result`. Finally, we print `result`, which should output `1`.

## Pseudo-Code
Here's the pseudo-code for calculating a mod b in Python:

```
1. Declare variables `a` and `b`
2. Assign values to `a` and `b`
3. Use the modulus operator to get the remainder of `a` divided by `b` and assign it to a variable `result`
4. Print the value of `result`
```

## Conclusion
Calculating a mod b in Python is very straightforward using the modulus operator. Just make sure you understand how the modulus operator works, and you'll be able to use it to solve more complex problems involving remainders.
