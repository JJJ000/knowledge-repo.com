---
title: The indentation style employed in Python for method calls that are chained
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The recommended style for chained method calls in Python is to use a hanging indent with each subsequent method call aligned with the first argument of the previous call.
---

**Contents**

[TOC]

Introduction
-------------

One of the many attractive features of Python is how readable and easy-to-write the code is. However, this can be a bit of a double-edged sword because different programmers may have different opinions on how to format their code. In this article, we will discuss the chained method calls indentation style in Python which is one of the style preferences a developer has to choose.

What is Chained method calls indentation style?
-----------------------------------------------

Chained method calls indentation style is a Python programming style that is used when methods are being called one after the other. This is most commonly seen when working with methods that return objects, specifically when the object has methods that can be called immediately. This style of formatting is called "chained methods" because it looks like a chain of method calls, each operating on the result of the previous method call.

Chained methods indentation style example:
------------------------------------------

```
result = MyObject()
                .get_first_part()
                .get_second_part()
                .concatenate_both_parts()
```

Advantages of Chained method calls indentation style
-----------------------------------------------------

1. Readability: Chained method calls indentation style makes the code easy to read and understand, especially when methods are related and their results are chained together.

2. Better organization: When reading and writing long chains of method calls, the chained method call style can help organize the methods in a more readable way.

3. Less code: This method reduces the number of lines of code needed to achieve the same result which also improves the readability of the code.

Disadvantages of Chained method calls indentation style
------------------------------------------------------

1. Debugging: When dealing with long chains of methods, it can be difficult to debug the code. Therefore this style must be used with caution.

2. Clarity: When chains of method calls become too long, they can become difficult to read and understand.

3. Inflexibility: Using chained methods can make your code more rigid by enforcing a certain structure of method calls that might not be flexible enough to meet changing requirements.

Conclusion
-----------
Chained method calls indentation style is a widely accepted style of writing Python code that helps keep code clean and organized. When dealing with long chains of methods, it is important to use this style judiciously and balance it with clarity and readability. This style makes the code more readable, less verbose, and easier to write.
