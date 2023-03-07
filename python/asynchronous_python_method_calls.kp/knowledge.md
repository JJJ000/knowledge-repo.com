---
title: What is meant by the phrase 'python's asynchronous method call'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Asynchronous method call in Python allows the program to continue executing while waiting for a function to complete instead of blocking the program until the function finishes.
---

**Contents**

[TOC]

Introduction

Asynchronous programming is a programming paradigm used for executing multiple tasks at the same time. It is the ability of a program to execute multiple tasks concurrently without waiting for the completion of one task before moving to the next task. In Python, asynchronous programming can be achieved using various modules like asyncio, concurrent.futures, etc. In this article, we will discuss the asynchronous method call in Python using the asyncio module.

What is an Asynchronous Method Call?

An asynchronous method call is a method that can be called without waiting for its completion. It allows the program to continue its execution without blocking the current thread. When a method is called asynchronously, the program immediately moves to the next statement without waiting for the method to complete its execution. Thus, the program can execute multiple methods concurrently.

Asynchronous Method Call using asyncio

Python asyncio module provides a way to write asynchronous code using coroutines. Coroutines are functions that can be paused and resumed. Asyncio provides an event loop that manages all the coroutines and schedules their execution. Here is an example of an asynchronous method call using asyncio:

``` python
import asyncio

async def my_method():
    print("My Method")

async def main():
    task = asyncio.create_task(my_method())
    print("Main Method")
    await task

asyncio.run(main())
```
In the above code, we defined a coroutine function, `my_method`. We created another coroutine function called `main` and scheduled the execution of the `my_method` using the `create_task` method. After we schedule the task, we print the `Main Method` message, and then await the completion of the `my_method` task using the `await` keyword.

Conclusion

Asynchronous method calls are very useful for writing programs that require multiple tasks to be executed concurrently. In Python, we can use the asyncio module to write asynchronous code using coroutines. We can schedule tasks using the `create_task` method and await the completion of tasks using the `await` keyword.
