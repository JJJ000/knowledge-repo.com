---
title: How to generate well-formatted columns using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can use the pandas library in Python to create nice column output, with options for formatting, sorting, and filtering the data.
---

**Contents**

[TOC]

## Introduction
In many applications, it is often necessary to print out data in a column format. Python provides several ways to do this, including using the `ljust()`, `rjust()`, `center()`, and `format()` methods. In this article, we will explore each of these methods and see how they can be used to create nice column output in Python.

## Using ljust(), rjust(), and center() methods
The `ljust()`, `rjust()`, and `center()` methods are used to align strings to the left, right, or center, respectively. These methods take an integer argument that specifies the width of the resulting string. If the original string is shorter than the specified width, the method adds spaces to make up the difference.

Here is an example code snippet that demonstrates the use of these methods:

```
name = 'John'
age = 25
occupation = 'Programmer'
print(name.ljust(10) + str(age).rjust(5) + occupation.center(20))
```

Output:
```
John          25         Programmer         
```

In this example, the `ljust(10)` method aligns the `name` string to the left with a width of 10 characters, `rjust(5)` aligns the `age` integer to the right with a width of 5 characters, and `center(20)` aligns the `occupation` string to the center with a width of 20 characters.

## Using the format() method
The `format()` method is a powerful and flexible way to format strings in Python. It allows you to insert values into placeholders, specify alignment, and control the width and precision of the output. Here is an example code snippet that demonstrates the use of the `format()` method to create column output:

```
name = 'John'
age = 25
occupation = 'Programmer'
print('{:<10}{:>5}{:^20}'.format(name, age, occupation))
```

Output:
```
John          25         Programmer         
```

In this example, we are using placeholders `{}` to indicate where the values should be inserted. The `<` and `>` characters before the width specification indicate left and right alignment, respectively. The `^` character indicates center alignment. The `10`, `5`, and `20` values indicate the width of the output for each value.

## Conclusion
Creating nice column output in Python is essential when presenting data to users. Using the `ljust()`, `rjust()`, `center()`, and `format()` methods, you can easily align strings and control the width and precision of the resulting columns. By understanding and using these methods, you can create visually appealing output that is easy to read and understand.
