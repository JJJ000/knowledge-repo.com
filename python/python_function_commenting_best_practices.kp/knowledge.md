---
title: How should functions be commented in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The proper way to comment functions in Python is by using the docstring, which includes a brief description of the function and its parameters.
---

**Contents**

[TOC]

Section 1: Overview of function commenting

Commenting functions is an important part of ensuring that your code is readable and easily understood by others. Commenting provides an explanation of what the function does, how it works, and what the inputs and outputs are. Comments can also provide additional context to help the reader understand the purpose of the function.

Section 2: Commenting guidelines for function signature

The function signature is the declaration of the function and is the first thing that a reader sees when looking at the function. When commenting the function signature, it is important to provide a brief explanation of what the function does and what inputs it expects. This should include the name of the function, its parameters, and its return type.

For example:

```
def calculate_area(radius: float) -> float:
    """
    Returns the area of a circle given the radius.

    :param radius: The radius of the circle.
    :return: The area of the circle.
    """
```

In this example, the comment provides a brief explanation of what the function does and what input it expects. It also notes that the function will return the area of the circle as a float.

Section 3: Commenting guidelines for function body

The function body contains the actual code that performs the function's task. When commenting the function body, it is important to explain each step of the process and what it is doing. Comments should be used to explain any complex or confusing code, and to provide clarity and context to the reader.

For example:

```
def calculate_area(radius: float) -> float:
    """
    Returns the area of a circle given the radius.

    :param radius: The radius of the circle.
    :return: The area of the circle.
    """
    # Calculate the area of the circle using the formula A = πr^2
    area = 3.141592653589793 * radius ** 2

    # Return the area
    return area
```

In this example, the comments explain the steps taken to calculate the area of the circle using the formula A = πr^2. The comment on the second line provides a brief overview of what the function does, while the comments within the function body explain in detail each step of the process.

Section 4: General commenting guidelines for functions

In general, when commenting functions in Python, it is important to follow these guidelines:

- Use descriptive function names that clearly explain what the function does.
- Use comments to explain any complex or confusing code.
- Provide a brief overview of the function at the top of the function signature.
- Explain the inputs and outputs of the function.
- Provide context or additional information that may help the reader understand the purpose of the function.
