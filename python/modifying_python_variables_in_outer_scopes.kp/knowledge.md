---
title: Can a variable that exists in an outer (enclosing) scope, but not in the global scope, be modified in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Yes, it is possible to modify a variable in Python that is in an outer (enclosing), but not global, scope by using the `nonlocal` keyword.
---

**Contents**

[TOC]

Yes, it is possible to modify a variable in Python that is in an outer (enclosing) scope using the `nonlocal` keyword. This feature was introduced in Python 3.

## Section 1: Understanding Scopes in Python

Python has four types of scopes:

- Local Scope
- Enclosing Scope
- Global Scope
- Built-in Scope

A variable declared inside a function is in the Local Scope, whereas a variable declared inside a nested function is in the Enclosing Scope. The Global Scope holds variables that are declared outside any function, and the Built-in Scope holds built-in functions and modules provided by Python.

## Section 2: Modifying Variables in Enclosing Scope

To modify a variable in an Enclosing Scope, we use the `nonlocal` keyword before that variable name. Here's an example:

```
def outer_function():
    x = "hello"
    def inner_function():
        nonlocal x
        x = "world"
    inner_function()
    print(x)

outer_function()
```

Output:
```
world
```

Here, we declare a variable `x` in the outer function and assign it the value `"hello"`. Next, we define a nested function `inner_function()` that modifies the value of `x` to `"world"`. Finally, we call `inner_function()` and print the value of `x`, which is `"world"`.

## Section 3: Limitations of `nonlocal`

The `nonlocal` keyword can only be used to modify variables in the immediate Enclosing Scope. If a variable is in a scope that is more than one level above the current scope, we cannot modify it using `nonlocal`. In such cases, it is better to use a different approach, like passing the variable as an argument to the nested function.

## Section 4: Conclusion

In conclusion, we can modify a variable in an Enclosing Scope using the `nonlocal` keyword in Python. It is a powerful feature that enables us to write more concise and reusable code. However, we should be aware of its limitations and use it judiciously.
