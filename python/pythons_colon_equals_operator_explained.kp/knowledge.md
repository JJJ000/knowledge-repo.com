---
title: What is the meaning of colon equal (=) in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Colon equal (=) in Python is known as the walrus operator, which assigns the result of an expression to a variable as well as returns it.
---

**Contents**

[TOC]

1. Definition
The colon equal (:=) in Python is a new operator introduced in Python 3.8. It is also known as the walrus operator. The colon equal operator is used to assign values to variables in expressions.

2. Usage
The colon equal (:=) operator is used to assign a new value to a variable within an expression. It allows the programmer to assign a value to a variable and also use the same variable in the same expression. 

3. Example
Here is an example that illustrates how to use the colon equal operator in Python:
```
# Assign value to variable x and print the value
x := 5
print(x)

# Use x in an expression to calculate the value of y
y := x * 2
print(y)

# Use x in a loop to iterate over a range of values
for i in range(1, x + 1):
    print(i)

# Use x in a conditional statement to print a message
if x > 3:
    print("x is greater than 3")
```

4. Benefits
The colon equal operator is useful for simplifying code and making it more readable. It allows the programmer to use the same variable in expressions and statements, which can reduce the number of lines of code that are needed. It also helps to avoid repetition of code and can improve the overall efficiency of the program.
