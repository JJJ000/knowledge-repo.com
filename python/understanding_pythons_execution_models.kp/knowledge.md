---
title: Comparison between coroutine, continuation, and generator
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Coroutine is a type of generator that allows for asynchronous programming, while continuation is a programming control structure used to manage the sequence of instructions, and generators are a type of function that can be paused and resumed.
---

**Contents**

[TOC]

# Coroutine
A coroutine is a special type of function that can pause its execution at certain points, allowing other code to run in the meantime, and then resume where it left off. This is similar to the way that cooperative multitasking works in operating systems. Coroutine functions are defined using the `async def` syntax in Python 3.5 and later. They are used extensively in asynchronous programming frameworks like asyncio and Trio, where they are used to implement tasks that can execute concurrently while still being able to cooperatively yield control when they need to wait for I/O or other tasks to complete.

# Continuation
A continuation is a mathematical concept that represents the future execution of a program. In Python, continuations are often used as a way of implementing non-local exits or backtracking in a program. They can be created using the `yield from` syntax in Python 3.3 and later. A continuation is a function that takes a single argument, which is a function that represents the rest of the computation that will be executed after the continuation returns. The continuation function saves the current state of the program and passes control to the rest of the computation, which may in turn call the continuation again at some later point, effectively rewinding the program to its earlier state.

# Generator
A generator is a special type of function that can produce a sequence of values lazily, on demand. Unlike regular functions, which execute from start to finish and return a single value, a generator can yield multiple values over time and then pause its execution until the next value is requested. This makes generators very useful for working with large data sets or infinite sequences, where it may not be practical to compute or store all of the values up front. In Python, generators are implemented using the `yield` keyword instead of `return`. They can also be defined as generator expressions or generator functions. Generator expressions are similar to list comprehensions, but they produce a generator object instead of a list. Generator functions are defined using the `def` keyword and the `yield` keyword, and can be called like regular functions.
