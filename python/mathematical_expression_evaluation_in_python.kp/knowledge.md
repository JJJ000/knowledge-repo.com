---
title: Assessing a mathematical calculation written in a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `eval()` function to evaluate a mathematical expression in a string in Python.
---

**Contents**

[TOC]

1. Introduction
In Python, it is possible to evaluate mathematical expressions in string form using the `eval()` function. The `eval()` function takes a string argument and returns the result of evaluating the expression contained within the string. However, it is important to exercise caution when using `eval()` as it can be a security risk if the input is not sanitized properly. In this tutorial, we will explore how to evaluate mathematical expressions in string form in Python while ensuring security and avoiding potential pitfalls.

2. Basic Usage
The `eval()` function can be used to evaluate simple mathematical expressions. For example:

```
result = eval("2 + 3")
print(result) # Output: 5
```

In the above code, we pass the string `"2 + 3"` to the `eval()` function, which returns the result of evaluating the expression `"2 + 3"`, which is `5`. 

3. Security Concerns
While using `eval()` can be useful for evaluating mathematical expressions, it is important to be aware of the security concerns associated with it. The `eval()` function can execute any code that is passed to it as a string, which means that it can be used to execute arbitrary code on the system. If the input to `eval()` is not sanitized properly, it can be used as a vector for injection attacks. For example, consider the following code:

```
user_input = input("Enter a mathematical expression: ")
result = eval(user_input)
```

If the user enters the string `"__import__('os').system('rm -rf /')"` as the input, the `eval()` function will execute the code to delete all files on the system. To prevent this, we can use the `ast.literal_eval()` function instead of `eval()`. The `ast.literal_eval()` function only evaluates expressions that contain literals and does not allow the execution of arbitrary code. For example:

```
import ast

user_input = input("Enter a mathematical expression: ")
try:
    result = ast.literal_eval(user_input)
    print(result)
except (SyntaxError, ValueError):
    print("Invalid input")
```

In the above code, we use the `ast.literal_eval()` function instead of `eval()` to evaluate the user's input. If the input is not a valid literal expression, an exception is raised, which we catch and handle gracefully.

4. Conclusion
In this tutorial, we have explored how to evaluate mathematical expressions in string form in Python while ensuring security and avoiding potential pitfalls. While `eval()` can be useful for simple use cases, it is important to properly sanitize user input and to use `ast.literal_eval()` instead of `eval()` whenever possible to prevent injection attacks. By following these guidelines, we can safely evaluate mathematical expressions in Python.
