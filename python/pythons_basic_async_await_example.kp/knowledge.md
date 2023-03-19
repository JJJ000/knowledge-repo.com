---
title: What is the most basic example of async/await in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Here`s an example

```
import asyncio

async def hello()
    print(`Hello`)
    await asyncio.sleep(1)
    print(`World`)

asyncio.run(hello())
```

This will print `Hello`, wait for one second, and then print `World`.
---

**Contents**

[TOC]

## Defining an async function

To use the `async/await` pattern in Python, we need to define an `async` function. These functions are similar to regular functions, but we prepend the `async` keyword to the function definition. Here's an example of a simple `async` function that will return a value after a delay:

```python
async def my_async_function():
    await asyncio.sleep(1)
    return "Done!"
```

## Calling the async function

To call an `async` function, we need to use the `await` keyword in front of the function call. Here's an example of how we could call the `my_async_function` example we defined earlier:

```python
async def main():
    result = await my_async_function()
    print(result)

# Run the asyncio event loop to execute our main function
asyncio.run(main())
```

Note that we need to wrap our call to `main` in the `asyncio.run()` function to start the event loop and execute the async code.

## Putting it all together

Here's the full example that combines the `my_async_function` definition and the `main` function into a complete program:

```python
import asyncio

async def my_async_function():
    await asyncio.sleep(1)
    return "Done!"

async def main():
    result = await my_async_function()
    print(result)

asyncio.run(main())
```

When we run this program, we'll see that it pauses for one second (due to the `await asyncio.sleep(1)` call), and then prints "Done!".
