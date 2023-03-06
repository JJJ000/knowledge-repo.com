---
title: What goal does the "send" function accomplish in Python generators?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The purpose of the `send` function on Python generators is to send a value back into the generator function and continue its execution from where it last yielded.
---

**Contents**

[TOC]

Introduction
Generators in Python are functions that return an iterable sequence of results, one at a time. The `send()` function is a method that can be used with generators to send values into the generator, which can then be processed further. In this article, we'll explore the purpose of the `send()` function on Python generators.

1. Sending values into a generator
One of the primary purposes of the `send()` function is to send values into a generator. This allows for two-way communication between the generator and the code that is using it. When a value is sent into the generator, it is received by the `yield` statement in the generator function. This allows the generator to process the value, and potentially modify its behavior based on the value that was sent.

2. Altering the state of a generator
Another purpose of the `send()` function is to alter the state of a generator. In Python, generators have internal state that is preserved between calls to the `next()` method. When a value is sent into the generator using the `send()` method, it can alter the internal state of the generator. This allows for more complex behavior in generators, such as maintaining a running total or modifying the behavior of the generator based on feedback from the code that is using it.

3. Handling exceptions in generators
The `send()` function can also be used to handle exceptions that occur within a generator. In Python, generators can raise exceptions just like any other function. However, because generators are typically used to produce large sequences of data, it can be useful to handle exceptions within the generator itself. The `send()` function can be used to catch exceptions that are raised within the generator and handle them in a more graceful way.

Conclusion
In conclusion, the `send()` function is a powerful tool that can be used to communicate with and modify the behavior of Python generators. It allows values to be sent into the generator, alters the state of the generator, and can handle exceptions that occur within the generator. By using the `send()` function effectively, developers can create more complex and efficient generator functions that are better suited to their specific use cases.
