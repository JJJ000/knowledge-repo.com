---
title: Rephrased asynchronous and awaitable programming in Python for "set it and forget it" approach
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: `Fire and forget` in Python async/await is a technique for running coroutines without waiting for their results or handling their exceptions.
---

**Contents**

[TOC]

## Introduction
"Fire and forget" refers to a programming pattern in which tasks can be executed asynchronously without the need to wait for the result. In Python, this can be achieved using the asyncio module and the async/await syntax.

## The async/await Syntax
The async/await syntax allows the developer to write asynchronous code in a synchronous style. Async functions are defined using the keyword `async` and can contain the `await` keyword to delegate tasks to other async functions.

## Implementing "Fire and Forget"
To implement "fire and forget" in Python using the asyncio module, we can define an async function that would spawn a new async task and then immediately return. The spawned task will run asynchronously in the background without blocking the main program.

## Example Code
Here's an example code snippet that demonstrates the "fire and forget" pattern using asyncio and Python:

```python
import asyncio

async def async_task():
    await asyncio.sleep(1)
    print("Async task finished")

async def fire_and_forget():
    asyncio.create_task(async_task())
    print("Task spawned, returning immediately")

asyncio.run(fire_and_forget())
```

In the code above, the `async_task()` function simulates some heavy work by sleeping for 1 second before printing a message. The `fire_and_forget()` function creates an async task using `asyncio.create_task()` and immediately returns. When the program is run, `fire_and_forget()` will print the message "Task spawned, returning immediately" and exit, while the `async_task()` function will run in the background and print the message "Async task finished" after 1 second.

That's how we can implement "fire and forget" in Python using async/await and the asyncio module.
