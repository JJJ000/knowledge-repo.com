---
title: Error in input() - nameerror name '...' is not defined
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The error occurs when a variable or function is referenced in the input() statement that has not been defined yet in Python.
---

**Contents**

[TOC]

Section 1: Explanation of the error

The input() function in Python is used to accept user input during the execution of a program. The error "NameError: name '...' is not defined" occurs when the value entered by the user is not assigned to a variable or is assigned to a variable but the variable is not defined in the program.

For example, consider the following code snippet:

number = input("Enter a number: ")
print("The number is:", x)

If the user enters a value, say 10, the program will try to print the value of the variable 'x' which has not been defined in the program. Hence, the 'NameError: name 'x' is not defined" error will be thrown.

Section 2: Fixing the error

To fix the "NameError: name '...' is not defined" error, we need to ensure that the value entered by the user is assigned to a variable and that the variable is defined in the program before it is used in any way.

For instance, let's modify the aforementioned code snippet to:

number = input("Enter a number: ")
print("The number is:", number)

In this modified program, the user's input is assigned to the 'number' variable, which is defined in the program. The value of 'number' is then printed to the console. Thus, the "NameError: name '...' is not defined" error will not appear.

Section 3: Handling invalid input

In addition to preventing "NameError: name '...' is not defined" errors, it is also essential to handle invalid input that may be entered by the user to avoid crashing the program.

For instance, consider this code snippet:

age = int(input("Enter your age: "))
print("Your age is", age)

If the user enters a non-integer value such as "twenty", a "ValueError: invalid literal for int() with base 10: 'twenty'" error will be raised. To avoid this, we can wrap the input() function inside a try-except block as follows:

try:
    age = int(input("Enter your age: "))
    print("Your age is", age)
except ValueError:
    print("Invalid age entered. Please enter a valid integer.")

In this program, if the user inputs a non-integer value, the program catches the ValueError exception, prints an error message to the console, and continues to run.

Section 4: Conclusion

This article has explained the "NameError: name '...' is not defined" error in Python, how to fix it, and how to handle invalid input. In summary, always ensure that any variable you use in your program is defined and assigned a value before using it. Also, use try-except blocks to handle invalid input and prevent your program from crashing.
