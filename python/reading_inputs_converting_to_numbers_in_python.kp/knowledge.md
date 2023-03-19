---
title: What is the method to read inputs as numerical values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the int() or float() function to convert the input string to an integer or float, respectively.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------
When we receive user inputs in Python, they are in the form of strings. However, if we want to perform numerical operations on the inputs, we need to convert them into numbers. In this tutorial, we will discuss how to read inputs as numbers in Python.

Section 2: Using the input() function and type casting
-------------------------------------------------------
In Python, we can read user inputs using the input() function. By default, the input() function reads the user input as a string. To convert the string input into an integer, we can use the int() function.

Example:
```python
num1 = int(input("Enter a number: "))
```
In the above code, we first read the user input using the input() function. The input is then converted into an integer using the int() function and stored in the variable num1.

Similarly, we can convert the user input into a float using the float() function.

Example:
```python
num2 = float(input("Enter a floating point number: "))
```
In the above code, the user input is read as a string using the input() function. The input is then converted into a floating-point number using the float() function and stored in the variable num2.

Section 3: Handling invalid inputs
----------------------------------
While reading user inputs as numbers, it is essential to handle invalid inputs. If the user enters a non-numeric value, the program will encounter an error. To avoid this, we can use exception handling.

Example:

```python
try:
    num3 = int(input("Enter a number: "))
except ValueError:
    print("Invalid input. Enter an integer.")
```
In the above code, we try to convert the input into an integer using the int() function. If the input is not an integer, a ValueError exception is raised. We handle the exception by printing a message and asking the user to input an integer.

Section 4: Conclusion
----------------------
In this tutorial, we discussed how to read user inputs as numbers in Python. We learned how to use the input() function and typecasting to convert the inputs into integers and floating-point numbers. We also discussed how to handle invalid inputs using exception handling. With this knowledge, you can create programs that can handle user inputs in a more sophisticated manner.
