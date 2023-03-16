---
title: What is the method to determine the highest (largest, greatest) value between two numbers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the built-in function max() and pass the two numbers as arguments.
---

**Contents**

[TOC]

# Introduction

One of the most basic and essential operations in programming is finding the maximum of two numbers. In Python, there are multiple ways to find the maximum of two numbers. In this tutorial, we will explore some of the commonly used methods to find the maximum of two numbers in Python.

## Method 1: Using the built-in max() function

The easiest way to find the maximum of two numbers in Python is to use the built-in max() function. The max() function takes any number of arguments and returns the maximum of all the arguments. We can use this function to find the maximum of two numbers as follows:

```python
a = 10
b = 20
max_number = max(a, b)
print(max_number)
```

In the above example, we have two numbers a=10 and b=20. We pass both these numbers as arguments to the max() function, and it returns the maximum of the two, which is 20.


## Method 2: Using if..else statement

Another way to find the maximum of two numbers in Python is to use the if..else statement. The logic is pretty simple: we compare the two numbers, and if the first number is greater than the second number, we assign the first number to a variable called max_number. Otherwise, we assign the second number to max_number variable as shown below:

```python
a = 10
b = 20

if a > b:
    max_number = a
else:
    max_number = b

print(max_number)
```

In the above code, we are comparing the two numbers a=10 and b=20. Since b is greater than a, the if block is not executed, and the value of max_number is assigned to b, which is the greater number.

## Method 3: Using the ternary operator

Python also supports the use of ternary operators, which is an efficient way of writing simple if..else statements in a single line. We can use a ternary operator to find the maximum of two numbers as follows:

```python
a = 10
b = 20

max_number = a if a > b else b

print(max_number)
```

In the above code, we are comparing the two numbers a=10 and b=20 using the ternary operator. Since b is greater than a, the value of max_number is assigned to b, which is the greater number.

## Conclusion

In this tutorial, we explored some of the commonly used methods to find the maximum of two numbers in Python. We used the built-in max() function, if..else statements, and ternary operators to find the maximum of two numbers, and we saw that all of these methods work well and give the correct output.
