---
title: Can you suggest a format to use for imports that span multiple lines?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Yes, there is a recommended format for multi-line imports in Python, which is to use parentheses and separate each import on a new line.
---

**Contents**

[TOC]

# Introduction

When working with large Python projects, it is common to have several import statements at the beginning of a file. When these import statements become too long, it can make the code difficult to read and modify. To solve this problem, multi-line imports can be used. In this article, we will discuss the recommended format for multi-line imports in Python.

## Import Statements

Import statements in Python are used to include external modules or functions into a program. In general, import statements are written at the top of a Python file, and multiple imports can be included in a single statement. Multi-line imports are used when the length of the import statement exceeds a predefined limit.

## Recommended Format

When using multi-line imports, it is important to follow a consistent format to improve the readability of the code. The recommended format for multi-line imports in Python is as follows:

```python
from module_name import (
    function_one,
    function_two,
    function_three,
)
```

This format includes the following elements:

- The from keyword is used to specify the module to import from.
- The module name is followed by an import statement in parentheses.
- Each function to be imported is included on a separate line, with a trailing comma after the last function.

## Why Use This Format?

There are several reasons why this format is recommended for multi-line imports in Python:

- It improves the readability of the code, making it easier to identify which modules and functions are being used.
- It makes it easier to add or remove functions from the import statement, since each function is on a separate line.
- It ensures that the import statement conforms to Python's style guide (PEP 8), which recommends a maximum line length of 79 characters.

## Conclusion

Multi-line imports are an important tool for managing imports in large Python projects. By following the recommended format, you can improve the readability and maintainability of your code. Remember to always adhere to Python's style guide and use a consistent format throughout your codebase.
