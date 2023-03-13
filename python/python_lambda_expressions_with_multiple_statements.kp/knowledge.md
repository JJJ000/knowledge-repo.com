---
title: Can a Python lambda expression contain more than one statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: No, a lambda expression can only have a single expression.
---

**Contents**

[TOC]

Yes, It is Possible to have multiple statements in a Python Lambda Expression

Python lambda expressions are known for their simplicity and brevity. However, they have certain limitations, and one of them is the inability to execute multiple statements. 

Section 1: A Brief Introduction to Lambda Expressions in Python

Lambda expressions are anonymous functions in Python that can be defined in a single line of code. These functions can take any number of arguments but can only have one expression. They are often used when a function is needed only once, and defining a named function would be too verbose. 

Example: 

```
add = lambda x, y: x + y
print(add(5, 10)) # Output: 15
```

Section 2: Limitations of Lambda Expressions in Python

The main limitation of lambda expressions is that they can only have one expression. This means that they cannot execute multiple statements, as opposed to a named function that can have multiple statements.

Example: 

```
def named_function():
    statement1()
    statement2()
    statement3()

named_function()
```

In the above example, named_function() executes three statements.

Section 3: How to Achieve Multiple Statements in a Lambda Expression in Python

To overcome the limitation of executing multiple statements in a lambda expression, you can create a sequence of statements using a semicolon (;) and enclose them in parentheses.

Example: 

```
multiply = lambda x: (
    print("The value of x is:", x),
    x * 2
)

print(multiply(5)) # Output: The value of x is: 5
                   #         10
```

In the above example, the lambda expression multiplies the input argument by 2 and also prints its value using multiple statements enclosed in parentheses. 

Section 4: Conclusion

In conclusion, although lambda expressions in Python have a limitation of executing only one expression, it is still possible to achieve multiple statements by enclosing them in parentheses and separating them with a semicolon.
